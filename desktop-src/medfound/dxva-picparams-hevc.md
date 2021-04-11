---
description: Stellt die Parameter auf Bild Ebene eines komprimierten Bilds für die hevc-Video Decodierung bereit.
ms.assetid: F73AE9CD-5BBC-4A9F-8D05-707AD5E2E92A
title: DXVA_PicParams_HEVC-Struktur (DXVA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXVA_PicParams_HEVC
api_type:
- HeaderDef
api_location:
- dxva.h
ms.openlocfilehash: cafcbf31a7d4b7fee84e6c695f1d0f0a1e0302ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127897"
---
# <a name="dxva_picparams_hevc-structure"></a>DXVA \_ picparser \_ hevc-Struktur

Stellt die Parameter auf Bild Ebene eines komprimierten Bilds für die hevc-Video Decodierung bereit.

## <a name="syntax"></a>Syntax


```C++
typedef struct _DXVA_PicParams_HEVC {
  USHORT             PicWidthInMinCbsY;
  USHORT             PicHeightInMinCbsY;
  union {
    struct {
      USHORT chroma_format_idc  :2;
      USHORT separate_colour_plane_flag   :1;
      USHORT bit_depth_luma_minus8   :3;
      USHORT bit_depth_chroma_minus8  :3;
      USHORT log2_max_pic_order_cnt_lsb_minus4  :4;
      USHORT NoPicReorderingFlag   :1;
      USHORT  NoBiPredFlag   :1;
      USHORT ReservedBits1     :1;
    };
    USHORT  wFormatAndSequenceInfoFlags;
  };
  DXVA_PicEntry_HEVC CurrPic;
  UCHAR              sps_max_dec_pic_buffering_minus1;
  UCHAR              log2_min_luma_coding_block_size_minus3;
  UCHAR              log2_diff_max_min_luma_coding_block_size;
  UCHAR              log2_min_transform_block_size_minus2;
  UCHAR              log2_diff_max_min_transform_block_size;
  UCHAR              max_transform_hierarchy_depth_inter;
  UCHAR              max_transform_hierarchy_depth_intra;
  UCHAR              num_short_term_ref_pic_sets;
  UCHAR              num_long_term_ref_pics_sps;
  UCHAR              num_ref_idx_l0_default_active_minus1;
  UCHAR              num_ref_idx_l1_default_active_minus1;
  CHAR               init_qp_minus26;
  UCHAR              ucNumDeltaPocsOfRefRpsIdx;
  USHORT             wNumBitsForShortTermRPSInSlice;
  USHORT             ReservedBits2;
  union {
    struct {
      UINT32 scaling_list_enabled_flag  :1;
      UINT32 amp_enabled_flag  :1;
      UINT32 sample_adaptive_offset_enabled_flag  :1;
      UINT32 pcm_enabled_flag   :1;
      UINT32 pcm_sample_bit_depth_luma_minus1   :4;
      UINT32 pcm_sample_bit_depth_chroma_minus1     :4;
      UINT32 log2_min_pcm_luma_coding_block_size_minus3    :2;
      UINT32 log2_diff_max_min_pcm_luma_coding_block_size  :2;
      UINT32 pcm_loop_filter_disabled_flag  :1;
      UINT32 long_term_ref_pics_present_flag   :1;
      UINT32 sps_temporal_mvp_enabled_flag  :1;
      UINT32 strong_intra_smoothing_enabled_flag   :1;
      UINT32 dependent_slice_segments_enabled_flag    :1;
      UINT32 output_flag_present_flag   :1;
      UINT32 num_extra_slice_header_bits    :3;
      UINT32 sign_data_hiding_enabled_flag  :1;
      UINT32 cabac_init_present_flag  :1;
      UINT32 ReservedBits3    :5;
    };
    UINT32             dwCodingParamToolFlags;
    union {
      struct {
        UINT32 constrained_intra_pred_flag  :1;
        UINT32 transform_skip_enabled_flag  :1;
        UINT32 cu_qp_delta_enabled_flag  :1;
        UINT32 pps_slice_chroma_qp_offsets_present_flag  :1;
        UINT32 weighted_pred_flag  :1;
        UINT32 weighted_bipred_flag  :1;
        UINT32 transquant_bypass_enabled_flag  :1;
        UINT32 tiles_enabled_flag   :1;
        UINT32 entropy_coding_sync_enabled_flag   :1;
        UINT32 uniform_spacing_flag    :1;
        UINT32 loop_filter_across_tiles_enabled_flag   :1;
        UINT32 pps_loop_filter_across_slices_enabled_flag  :1;
        UINT32 deblocking_filter_override_enabled_flag  :1;
        UINT32 pps_deblocking_filter_disabled_flag  :1;
        UINT32 lists_modification_present_flag  :1;
        UINT32 slice_segment_header_extension_present_flag  :1;
        UINT32 IrapPicFlag  :1;
        UINT32 IdrPicFlag     :1;
        UINT32 IntraPicFlag   :1;
        UINT32 ReservedBits4     :13;
      };
      UINT32   dwCodingSettingPicturePropertyFlags;
    };
    CHAR               pps_cb_qp_offset;
    CHAR               pps_cr_qp_offset;
    UCHAR              num_tile_columns_minus1;
    UCHAR              num_tile_rows_minus1;
    USHORT             column_width_minus1[19];
    USHORT             row_height_minus1[21];
    UCHAR              diff_cu_qp_delta_depth;
    CHAR               pps_beta_offset_div2;
    CHAR               pps_tc_offset_div2;
    UCHAR              log2_parallel_merge_level_minus2;
    INT                CurrPicOrderCntVal;
    DXVA_PicEntry_HEVC RefPicList[15];
    UCHAR              ReservedBits5;
    INT                PicOrderCntValList[15];
    UCHAR              RefPicSetStCurrBefore[8];
    UCHAR              RefPicSetStCurrAfter[8];
    UCHAR              RefPicSetLtCurr[8];
    USHORT             ReservedBits6;
    USHORT             ReservedBits7;
    UINT               StatusReportFeedbackNumber;
  };
} DXVA_PicParams_HEVC, *PDXVA_PicParams_HEVC;
```



## <a name="members"></a>Member

<dl> <dt>

**Picwidthinmincbsy**
</dt> <dd></dd> <dt>

**Picheightinmincbsy**
</dt> <dd></dd> <dt>

**Chroma- \_ Format \_ IDC**
</dt> <dd></dd> <dt>

**separates \_ Flag der Farbraum \_ \_** 
</dt> <dd></dd> <dt>

**Bittiefe- \_ \_ Luma- \_ Minus8** 
</dt> <dd></dd> <dt>

**\_Bittiefe \_ Chroma \_ Minus8**
</dt> <dd></dd> <dt>

**log2 \_ Max. \_ PIC \_ Order \_ CNT- \_ lsb \_ minus4**
</dt> <dd></dd> <dt>

**Nopikreorderingflag** 
</dt> <dd></dd> <dt>

 **Nobipredflag** 
</dt> <dd></dd> <dt>

**ReservedBits1** 
</dt> <dd></dd> <dt>

**wformatandsequenceingefoflags**
</dt> <dd></dd> <dt>

**Currpic**
</dt> <dd></dd> <dt>

**maximal zulässige SPS- \_ \_ \_ \_ \_ minus1**
</dt> <dd></dd> <dt>

**log2 \_ Min. \_ Luma- \_ Codierungs \_ Block \_ Größe \_ minus3**
</dt> <dd></dd> <dt>

**log2 \_ diff \_ Max \_ min Min. Größe für die \_ \_ \_ Codeblock \_ Größe**
</dt> <dd></dd> <dt>

**log2 \_ Min. \_ Transformations \_ Block \_ Größe \_ minus2**
</dt> <dd></dd> <dt>

**log2 \_ diff \_ Maximale \_ minimale \_ \_ Block \_ Größe für die Transformation**
</dt> <dd></dd> <dt>

**maximale \_ Transformations \_ \_ hierarchientiefe \_ zwischen**
</dt> <dd></dd> <dt>

**maximale \_ Tiefe der Transformations \_ Hierarchie in \_ \_**
</dt> <dd></dd> <dt>

**Anzahl \_ kurzfristiger Verweis- \_ \_ \_ \_ pipsets**
</dt> <dd></dd> <dt>

**NUM \_ langfristige \_ \_ ref- \_ Bilder \_ SPS**
</dt> <dd></dd> <dt>

**NUM \_ ref \_ IDX \_ L0 \_ standardmäßig \_ aktiv \_ minus1**
</dt> <dd></dd> <dt>

**NUM \_ ref \_ IDX \_ L1 \_ Standard \_ aktiv \_ minus1**
</dt> <dd></dd> <dt>

**init \_ Abfrage Prozessor \_ minus26**
</dt> <dd></dd> <dt>

**ucnumdelta tapocsofrefrpsidx**
</dt> <dd></dd> <dt>

**wnumbizforshorttermrpsinslice**
</dt> <dd></dd> <dt>

**ReservedBits2**
</dt> <dd></dd> <dt>

**\_Flag für \_ aktivierte Skalierungs Liste \_**
</dt> <dd></dd> <dt>

**amp- \_ aktiviertes \_ Flag**
</dt> <dd></dd> <dt>

**Beispiel für \_ Adaptives \_ Offsets \_ aktiviert \_**
</dt> <dd></dd> <dt>

**PCM- \_ aktiviertes \_ Flag** 
</dt> <dd></dd> <dt>

**PCM \_ Sample \_ Bit \_ Tiefe \_ Luma \_ minus1** 
</dt> <dd></dd> <dt>

**PCM \_ Sample \_ \_ Bittiefe \_ Chroma \_ minus1** 
</dt> <dd></dd> <dt>

**log2 \_ Min. \_ PCM-Größe für \_ \_ Codierungs \_ Blöcke \_ \_ minus3** 
</dt> <dd></dd> <dt>

**log2 \_ diff \_ Max \_ Min. \_ PCM- \_ \_ Größe Codierungs \_ Block \_ Größe**
</dt> <dd></dd> <dt>

**\_Flag für \_ \_ deaktiviertes PCM-Schleifen \_**
</dt> <dd></dd> <dt>

**Flag für langfristige \_ \_ ref- \_ Bilder \_ vorhanden \_** 
</dt> <dd></dd> <dt>

**SPS- \_ Flag für temporäres \_ MVP \_ aktiviert \_**
</dt> <dd></dd> <dt>

**Flag für starke \_ \_ interglättung \_ aktiviert \_** 
</dt> <dd></dd> <dt>

**Flag für abhängige \_ Slice- \_ Segmente \_ aktiviert \_** 
</dt> <dd></dd> <dt>

**\_Flag für ausgabeflag \_ vorhanden \_** 
</dt> <dd></dd> <dt>

**NUM \_ zusätzliche \_ Slice- \_ Header \_ Bits** 
</dt> <dd></dd> <dt>

**Flag zum Ausblenden von signierten \_ Daten \_ \_ \_**
</dt> <dd></dd> <dt>

**CABAC \_ Init \_ Present- \_ Flag**
</dt> <dd></dd> <dt>

**ReservedBits3** 
</dt> <dd></dd> <dt>

**dwcodingparamtoolflags**
</dt> <dd></dd> <dt>

**eingeschränkter \_ Intra \_ -Pred- \_ Flag**
</dt> <dd></dd> <dt>

**Flag zum Aktivieren der Transformation für \_ Skip \_ \_**
</dt> <dd></dd> <dt>

**Cu- \_ Abfrage Prozessor- \_ Delta \_ aktiviertes \_ Flag**
</dt> <dd></dd> <dt>

**PPS \_ Slice \_ Chroma- \_ Abfrage Prozessor- \_ Offsets- \_ \_ Flag vorhanden**
</dt> <dd></dd> <dt>

**gewichtetes \_ Pred- \_ Flag**
</dt> <dd></dd> <dt>

**gewichtetes \_ bipred- \_ Flag**
</dt> <dd></dd> <dt>

**\_ \_ Flag für aktivierte transquant-Umgehung \_**
</dt> <dd></dd> <dt>

**Kacheln \_ aktiviert, \_ Flag** 
</dt> <dd></dd> <dt>

**Entropie \_ \_ codierungssynchronisierungsflag \_ aktiviert \_** 
</dt> <dd></dd> <dt>

**Flag für einheitliches \_ Abstand \_** 
</dt> <dd></dd> <dt>

**Schleifen \_ Filter \_ über \_ Kacheln \_ aktiviert, \_ Flag** 
</dt> <dd></dd> <dt>

**\_ \_ \_ über \_ Slices \_ aktivierte \_ Flags-Schleifen Filter**
</dt> <dd></dd> <dt>

**Flag zum Aufheben der Blockierung des \_ Filters wird \_ \_ aktiviert \_**
</dt> <dd></dd> <dt>

**\_ \_ \_ aktiviertes Flag zum Deaktivieren des PPS-Filters \_**
</dt> <dd></dd> <dt>

**listet \_ \_ modifizierungsflag \_**
</dt> <dd></dd> <dt>

**Flag für das vorhanden sein des Slice- \_ Segment \_ Headers \_ \_ \_**
</dt> <dd></dd> <dt>

**Irappicflag**
</dt> <dd></dd> <dt>

**Idrpicflag** 
</dt> <dd></dd> <dt>

**"Inner picflag"** 
</dt> <dd></dd> <dt>

**ReservedBits4** 
</dt> <dd></dd> <dt>

**dwcodingsettingpicturepropertyflags**
</dt> <dd></dd> <dt>

**PPS \_ CB- \_ Abfrage Prozessor- \_ Offset**
</dt> <dd></dd> <dt>

**PPS \_ CR- \_ Abfrage Prozessor- \_ Offset**
</dt> <dd></dd> <dt>

**NUM- \_ Kachel \_ Spalten \_ minus1**
</dt> <dd></dd> <dt>

**NUM- \_ Kachel \_ Zeilen \_ minus1**
</dt> <dd></dd> <dt>

**Spalten \_ Breite \_ minus1**
</dt> <dd></dd> <dt>

**Zeilen \_ Höhe \_ minus1**
</dt> <dd></dd> <dt>

**differenzielle \_ Cu- \_ Abfrage Prozessor- \_ Delta \_ Tiefe**
</dt> <dd></dd> <dt>

**PPS \_ Beta \_ Offset \_ div2**
</dt> <dd></dd> <dt>

**PPS- \_ TC- \_ Offset \_ div2**
</dt> <dd></dd> <dt>

**log2 \_ parallel \_ Merge \_ Level \_ minus2**
</dt> <dd></dd> <dt>

**Currpicordercntval**
</dt> <dd></dd> <dt>

**Refpiclist**
</dt> <dd></dd> <dt>

**ReservedBits5**
</dt> <dd></dd> <dt>

**Picordercntvallist**
</dt> <dd></dd> <dt>

**Ref-setstcurrbefore**
</dt> <dd></dd> <dt>

**Ref-setstcurrrafter**
</dt> <dd></dd> <dt>

**Ref-setltcurrr**
</dt> <dd></dd> <dt>

**ReservedBits6**
</dt> <dd></dd> <dt>

**ReservedBits7**
</dt> <dd></dd> <dt>

**Status Report feedbacknumber**
</dt> <dd></dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Nur Desktop-Apps Windows 8.1\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 R2 \[ -Desktop-Apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>DXVA. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation Strukturen](media-foundation-structures.md)
</dt> </dl>

 

 




