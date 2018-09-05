# rdp_16s_v16_sp_ManualAdjustment


**rdp_16s_v16s_sp_ManualAdjustment201808.fa** is a manually reviewed and adjusted database for taxonomy classification based on 16S rRNA gene sequences. This database is modified from [rdp_16s_v16s_sp.fa](https://www.drive5.com/sintax/rdp_16s_v16_sp.fa.gz), which is a RDP training set with species names.

**rdp_16s_v16s_sp_adjustment_list.tsv** details a total of 902 taxonomy label changes. 

In brief, the following types of adjustement were made:

1. Two multiple-parent issues in the original RDP training set were fiexed (s:Nitrospirillum_amazonense has parents g:Nitrospirillum and g:Azospirillum; s:Methanolacinia_petrolearia has parents g:Methanolacinia and g:Methanoplanus).

2. The format of taxonomy in the origianl RDP training set is "d:xxxxx,p:xxxxx,c:xxxxx,o:xxxxx,f:xxxxx,g:xxxxx(,s:xxxxx)", but "c:xxxxx", "o:xxxxx" and "f:xxxxx" are missing in some taxonomy lables. The missing information is firstly filled by searching [LPSN](http://www.bacterio.net/-classifphyla.html#cowdria), [wikispecies](https://species.wikimedia.org/wiki/Main_Page), and other resources like [UniProt](https://www.uniprot.org/taxonomy), [NamesforLife](https://www.namesforlife.com) and [MicrobeWiki](https://microbewiki.kenyon.edu/index.php/MicrobeWiki) if LPSN is in conflict with wikispecies; if no information could be found from LPSN and wikispecies, "xxxxx_incertae_sedis" is used (with xxxxx being the taxon name at the nearest higher level availiable).

   Examples: 
*tax=d:Bacteria,p:"Proteobacteria",c:Gammaproteobacteria,o:Gammaproteobacteria_incertae_sedis,g:Pleionea,s:Pleionea_mediterranea* is adjusted to *tax=d:Bacteria,p:"Proteobacteria",c:Gammaproteobacteria,o:Oceanospirillales,f:Alcanivoracaceae,g:Pleionea,s:Pleionea_mediterranea*; 
*tax=d:Bacteria,p:SR1,g:SR1_genera_incertae_sedis* is adjusted to *tax=d:Bacteria,p:SR1,c:SR1_incertae_sedis,o:SR1_incertae_sedis,f:SR1_incertae_sedis,g:SR1_genera_incertae_sedis*.

3. A few taxonomy labels were adjusted with reference to multiple resources mentioned above.

   Example:
*tax=d:Bacteria,p:"Bacteroidetes",c:Sphingobacteriia,o:"Sphingobacteriales",f:Chitinophagaceae,g:Gracilimonas* is adjusted to *tax=d:Bacteria,p:Balneolaeota,c:Balneolia,o:Balneolales,f:Balneolace*.

For comments and questions, please contact Li Zhang <li.zhang2016#outlook.com> or Zhilong Jia <zhilongjia#gmail.com>.
