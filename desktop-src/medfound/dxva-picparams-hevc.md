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
# <a name="dxva_picparams_hevc-structure"></a><span data-ttu-id="07e2e-103">DXVA \_ picparser \_ hevc-Struktur</span><span class="sxs-lookup"><span data-stu-id="07e2e-103">DXVA\_PicParams\_HEVC structure</span></span>

<span data-ttu-id="07e2e-104">Stellt die Parameter auf Bild Ebene eines komprimierten Bilds für die hevc-Video Decodierung bereit.</span><span class="sxs-lookup"><span data-stu-id="07e2e-104">Provides the picture-level parameters of a compressed picture for HEVC video decoding.</span></span>

## <a name="syntax"></a><span data-ttu-id="07e2e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="07e2e-105">Syntax</span></span>


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



## <a name="members"></a><span data-ttu-id="07e2e-106">Member</span><span class="sxs-lookup"><span data-stu-id="07e2e-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="07e2e-107">**Picwidthinmincbsy**</span><span class="sxs-lookup"><span data-stu-id="07e2e-107">**PicWidthInMinCbsY**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="07e2e-108">**Picheightinmincbsy**</span><span class="sxs-lookup"><span data-stu-id="07e2e-108">**PicHeightInMinCbsY**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="07e2e-109">**Chroma- \_ Format \_ IDC**</span><span class="sxs-lookup"><span data-stu-id="07e2e-109">**chroma\_format\_idc**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="07e2e-110">**separates \_ Flag der Farbraum \_ \_**</span><span class="sxs-lookup"><span data-stu-id="07e2e-110">**separate\_colour\_plane\_flag**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="07e2e-111">**Bittiefe- \_ \_ Luma- \_ Minus8**</span><span class="sxs-lookup"><span data-stu-id="07e2e-111">**bit\_depth\_luma\_minus8**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="07e2e-112">**\_Bittiefe \_ Chroma \_ Minus8**</span><span class="sxs-lookup"><span data-stu-id="07e2e-112">**bit\_depth\_chroma\_minus8**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="07e2e-113">**log2 \_ Max. \_ PIC \_ Order \_ CNT- \_ lsb \_ minus4**</span><span class="sxs-lookup"><span data-stu-id="07e2e-113">**log2\_max\_pic\_order\_cnt\_lsb\_minus4**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="07e2e-114">**Nopikreorderingflag**</span><span class="sxs-lookup"><span data-stu-id="07e2e-114">**NoPicReorderingFlag**</span></span> 
</dt> <dd></dd> <dt>

 <span data-ttu-id="07e2e-115">**Nobipredflag**</span><span class="sxs-lookup"><span data-stu-id="07e2e-115">**NoBiPredFlag**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="07e2e-116">**ReservedBits1**</span><span class="sxs-lookup"><span data-stu-id="07e2e-116">**ReservedBits1**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="07e2e-117">**wformatandsequenceingefoflags**</span><span class="sxs-lookup"><span data-stu-id="07e2e-117">**wFormatAndSequenceInfoFlags**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="07e2e-118">**Currpic**</span><span class="sxs-lookup"><span data-stu-id="07e2e-118">**CurrPic**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="07e2e-119">**maximal zulässige SPS- \_ \_ \_ \_ \_ minus1**</span><span class="sxs-lookup"><span data-stu-id="07e2e-119">**sps\_max\_dec\_pic\_buffering\_minus1**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="07e2e-120">**log2 \_ Min. \_ Luma- \_ Codierungs \_ Block \_ Größe \_ minus3**</span><span class="sxs-lookup"><span data-stu-id="07e2e-120">**log2\_min\_luma\_coding\_block\_size\_minus3**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="07e2e-121">**log2 \_ diff \_ Max \_ min Min. Größe für die \_ \_ \_ Codeblock \_ Größe**</span><span class="sxs-lookup"><span data-stu-id="07e2e-121">**log2\_diff\_max\_min\_luma\_coding\_block\_size**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="07e2e-122">**log2 \_ Min. \_ Transformations \_ Block \_ Größe \_ minus2**</span><span class="sxs-lookup"><span data-stu-id="07e2e-122">**log2\_min\_transform\_block\_size\_minus2**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="07e2e-123">**log2 \_ diff \_ Maximale \_ minimale \_ \_ Block \_ Größe für die Transformation**</span><span class="sxs-lookup"><span data-stu-id="07e2e-123">**log2\_diff\_max\_min\_transform\_block\_size**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="07e2e-124">**maximale \_ Transformations \_ \_ hierarchientiefe \_ zwischen**</span><span class="sxs-lookup"><span data-stu-id="07e2e-124">**max\_transform\_hierarchy\_depth\_inter**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="07e2e-125">**maximale \_ Tiefe der Transformations \_ Hierarchie in \_ \_**</span><span class="sxs-lookup"><span data-stu-id="07e2e-125">**max\_transform\_hierarchy\_depth\_intra**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="07e2e-126">**Anzahl \_ kurzfristiger Verweis- \_ \_ \_ \_ pipsets**</span><span class="sxs-lookup"><span data-stu-id="07e2e-126">**num\_short\_term\_ref\_pic\_sets**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="07e2e-127">**NUM \_ langfristige \_ \_ ref- \_ Bilder \_ SPS**</span><span class="sxs-lookup"><span data-stu-id="07e2e-127">**num\_long\_term\_ref\_pics\_sps**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="07e2e-128">**NUM \_ ref \_ IDX \_ L0 \_ standardmäßig \_ aktiv \_ minus1**</span><span class="sxs-lookup"><span data-stu-id="07e2e-128">**num\_ref\_idx\_l0\_default\_active\_minus1**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="07e2e-129">**NUM \_ ref \_ IDX \_ L1 \_ Standard \_ aktiv \_ minus1**</span><span class="sxs-lookup"><span data-stu-id="07e2e-129">**num\_ref\_idx\_l1\_default\_active\_minus1**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="07e2e-130">**init \_ Abfrage Prozessor \_ minus26**</span><span class="sxs-lookup"><span data-stu-id="07e2e-130">**init\_qp\_minus26**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="07e2e-131">**ucnumdelta tapocsofrefrpsidx**</span><span class="sxs-lookup"><span data-stu-id="07e2e-131">**ucNumDeltaPocsOfRefRpsIdx**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="07e2e-132">**wnumbizforshorttermrpsinslice**</span><span class="sxs-lookup"><span data-stu-id="07e2e-132">**wNumBitsForShortTermRPSInSlice**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="07e2e-133">**ReservedBits2**</span><span class="sxs-lookup"><span data-stu-id="07e2e-133">**ReservedBits2**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="07e2e-134">**\_Flag für \_ aktivierte Skalierungs Liste \_**</span><span class="sxs-lookup"><span data-stu-id="07e2e-134">**scaling\_list\_enabled\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="07e2e-135">**amp- \_ aktiviertes \_ Flag**</span><span class="sxs-lookup"><span data-stu-id="07e2e-135">**amp\_enabled\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="07e2e-136">**Beispiel für \_ Adaptives \_ Offsets \_ aktiviert \_**</span><span class="sxs-lookup"><span data-stu-id="07e2e-136">**sample\_adaptive\_offset\_enabled\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="07e2e-137">**PCM- \_ aktiviertes \_ Flag**</span><span class="sxs-lookup"><span data-stu-id="07e2e-137">**pcm\_enabled\_flag**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="07e2e-138">**PCM \_ Sample \_ Bit \_ Tiefe \_ Luma \_ minus1**</span><span class="sxs-lookup"><span data-stu-id="07e2e-138">**pcm\_sample\_bit\_depth\_luma\_minus1**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="07e2e-139">**PCM \_ Sample \_ \_ Bittiefe \_ Chroma \_ minus1**</span><span class="sxs-lookup"><span data-stu-id="07e2e-139">**pcm\_sample\_bit\_depth\_chroma\_minus1**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="07e2e-140">**log2 \_ Min. \_ PCM-Größe für \_ \_ Codierungs \_ Blöcke \_ \_ minus3**</span><span class="sxs-lookup"><span data-stu-id="07e2e-140">**log2\_min\_pcm\_luma\_coding\_block\_size\_minus3**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="07e2e-141">**log2 \_ diff \_ Max \_ Min. \_ PCM- \_ \_ Größe Codierungs \_ Block \_ Größe**</span><span class="sxs-lookup"><span data-stu-id="07e2e-141">**log2\_diff\_max\_min\_pcm\_luma\_coding\_block\_size**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="07e2e-142">**\_Flag für \_ \_ deaktiviertes PCM-Schleifen \_**</span><span class="sxs-lookup"><span data-stu-id="07e2e-142">**pcm\_loop\_filter\_disabled\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="07e2e-143">**Flag für langfristige \_ \_ ref- \_ Bilder \_ vorhanden \_**</span><span class="sxs-lookup"><span data-stu-id="07e2e-143">**long\_term\_ref\_pics\_present\_flag**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="07e2e-144">**SPS- \_ Flag für temporäres \_ MVP \_ aktiviert \_**</span><span class="sxs-lookup"><span data-stu-id="07e2e-144">**sps\_temporal\_mvp\_enabled\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="07e2e-145">**Flag für starke \_ \_ interglättung \_ aktiviert \_**</span><span class="sxs-lookup"><span data-stu-id="07e2e-145">**strong\_intra\_smoothing\_enabled\_flag**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="07e2e-146">**Flag für abhängige \_ Slice- \_ Segmente \_ aktiviert \_**</span><span class="sxs-lookup"><span data-stu-id="07e2e-146">**dependent\_slice\_segments\_enabled\_flag**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="07e2e-147">**\_Flag für ausgabeflag \_ vorhanden \_**</span><span class="sxs-lookup"><span data-stu-id="07e2e-147">**output\_flag\_present\_flag**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="07e2e-148">**NUM \_ zusätzliche \_ Slice- \_ Header \_ Bits**</span><span class="sxs-lookup"><span data-stu-id="07e2e-148">**num\_extra\_slice\_header\_bits**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="07e2e-149">**Flag zum Ausblenden von signierten \_ Daten \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="07e2e-149">**sign\_data\_hiding\_enabled\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="07e2e-150">**CABAC \_ Init \_ Present- \_ Flag**</span><span class="sxs-lookup"><span data-stu-id="07e2e-150">**cabac\_init\_present\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="07e2e-151">**ReservedBits3**</span><span class="sxs-lookup"><span data-stu-id="07e2e-151">**ReservedBits3**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="07e2e-152">**dwcodingparamtoolflags**</span><span class="sxs-lookup"><span data-stu-id="07e2e-152">**dwCodingParamToolFlags**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="07e2e-153">**eingeschränkter \_ Intra \_ -Pred- \_ Flag**</span><span class="sxs-lookup"><span data-stu-id="07e2e-153">**constrained\_intra\_pred\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="07e2e-154">**Flag zum Aktivieren der Transformation für \_ Skip \_ \_**</span><span class="sxs-lookup"><span data-stu-id="07e2e-154">**transform\_skip\_enabled\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="07e2e-155">**Cu- \_ Abfrage Prozessor- \_ Delta \_ aktiviertes \_ Flag**</span><span class="sxs-lookup"><span data-stu-id="07e2e-155">**cu\_qp\_delta\_enabled\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="07e2e-156">**PPS \_ Slice \_ Chroma- \_ Abfrage Prozessor- \_ Offsets- \_ \_ Flag vorhanden**</span><span class="sxs-lookup"><span data-stu-id="07e2e-156">**pps\_slice\_chroma\_qp\_offsets\_present\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="07e2e-157">**gewichtetes \_ Pred- \_ Flag**</span><span class="sxs-lookup"><span data-stu-id="07e2e-157">**weighted\_pred\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="07e2e-158">**gewichtetes \_ bipred- \_ Flag**</span><span class="sxs-lookup"><span data-stu-id="07e2e-158">**weighted\_bipred\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="07e2e-159">**\_ \_ Flag für aktivierte transquant-Umgehung \_**</span><span class="sxs-lookup"><span data-stu-id="07e2e-159">**transquant\_bypass\_enabled\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="07e2e-160">**Kacheln \_ aktiviert, \_ Flag**</span><span class="sxs-lookup"><span data-stu-id="07e2e-160">**tiles\_enabled\_flag**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="07e2e-161">**Entropie \_ \_ codierungssynchronisierungsflag \_ aktiviert \_**</span><span class="sxs-lookup"><span data-stu-id="07e2e-161">**entropy\_coding\_sync\_enabled\_flag**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="07e2e-162">**Flag für einheitliches \_ Abstand \_**</span><span class="sxs-lookup"><span data-stu-id="07e2e-162">**uniform\_spacing\_flag**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="07e2e-163">**Schleifen \_ Filter \_ über \_ Kacheln \_ aktiviert, \_ Flag**</span><span class="sxs-lookup"><span data-stu-id="07e2e-163">**loop\_filter\_across\_tiles\_enabled\_flag**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="07e2e-164">**\_ \_ \_ über \_ Slices \_ aktivierte \_ Flags-Schleifen Filter**</span><span class="sxs-lookup"><span data-stu-id="07e2e-164">**pps\_loop\_filter\_across\_slices\_enabled\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="07e2e-165">**Flag zum Aufheben der Blockierung des \_ Filters wird \_ \_ aktiviert \_**</span><span class="sxs-lookup"><span data-stu-id="07e2e-165">**deblocking\_filter\_override\_enabled\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="07e2e-166">**\_ \_ \_ aktiviertes Flag zum Deaktivieren des PPS-Filters \_**</span><span class="sxs-lookup"><span data-stu-id="07e2e-166">**pps\_deblocking\_filter\_disabled\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="07e2e-167">**listet \_ \_ modifizierungsflag \_**</span><span class="sxs-lookup"><span data-stu-id="07e2e-167">**lists\_modification\_present\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="07e2e-168">**Flag für das vorhanden sein des Slice- \_ Segment \_ Headers \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="07e2e-168">**slice\_segment\_header\_extension\_present\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="07e2e-169">**Irappicflag**</span><span class="sxs-lookup"><span data-stu-id="07e2e-169">**IrapPicFlag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="07e2e-170">**Idrpicflag**</span><span class="sxs-lookup"><span data-stu-id="07e2e-170">**IdrPicFlag**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="07e2e-171">**"Inner picflag"**</span><span class="sxs-lookup"><span data-stu-id="07e2e-171">**IntraPicFlag**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="07e2e-172">**ReservedBits4**</span><span class="sxs-lookup"><span data-stu-id="07e2e-172">**ReservedBits4**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="07e2e-173">**dwcodingsettingpicturepropertyflags**</span><span class="sxs-lookup"><span data-stu-id="07e2e-173">**dwCodingSettingPicturePropertyFlags**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="07e2e-174">**PPS \_ CB- \_ Abfrage Prozessor- \_ Offset**</span><span class="sxs-lookup"><span data-stu-id="07e2e-174">**pps\_cb\_qp\_offset**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="07e2e-175">**PPS \_ CR- \_ Abfrage Prozessor- \_ Offset**</span><span class="sxs-lookup"><span data-stu-id="07e2e-175">**pps\_cr\_qp\_offset**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="07e2e-176">**NUM- \_ Kachel \_ Spalten \_ minus1**</span><span class="sxs-lookup"><span data-stu-id="07e2e-176">**num\_tile\_columns\_minus1**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="07e2e-177">**NUM- \_ Kachel \_ Zeilen \_ minus1**</span><span class="sxs-lookup"><span data-stu-id="07e2e-177">**num\_tile\_rows\_minus1**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="07e2e-178">**Spalten \_ Breite \_ minus1**</span><span class="sxs-lookup"><span data-stu-id="07e2e-178">**column\_width\_minus1**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="07e2e-179">**Zeilen \_ Höhe \_ minus1**</span><span class="sxs-lookup"><span data-stu-id="07e2e-179">**row\_height\_minus1**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="07e2e-180">**differenzielle \_ Cu- \_ Abfrage Prozessor- \_ Delta \_ Tiefe**</span><span class="sxs-lookup"><span data-stu-id="07e2e-180">**diff\_cu\_qp\_delta\_depth**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="07e2e-181">**PPS \_ Beta \_ Offset \_ div2**</span><span class="sxs-lookup"><span data-stu-id="07e2e-181">**pps\_beta\_offset\_div2**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="07e2e-182">**PPS- \_ TC- \_ Offset \_ div2**</span><span class="sxs-lookup"><span data-stu-id="07e2e-182">**pps\_tc\_offset\_div2**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="07e2e-183">**log2 \_ parallel \_ Merge \_ Level \_ minus2**</span><span class="sxs-lookup"><span data-stu-id="07e2e-183">**log2\_parallel\_merge\_level\_minus2**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="07e2e-184">**Currpicordercntval**</span><span class="sxs-lookup"><span data-stu-id="07e2e-184">**CurrPicOrderCntVal**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="07e2e-185">**Refpiclist**</span><span class="sxs-lookup"><span data-stu-id="07e2e-185">**RefPicList**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="07e2e-186">**ReservedBits5**</span><span class="sxs-lookup"><span data-stu-id="07e2e-186">**ReservedBits5**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="07e2e-187">**Picordercntvallist**</span><span class="sxs-lookup"><span data-stu-id="07e2e-187">**PicOrderCntValList**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="07e2e-188">**Ref-setstcurrbefore**</span><span class="sxs-lookup"><span data-stu-id="07e2e-188">**RefPicSetStCurrBefore**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="07e2e-189">**Ref-setstcurrrafter**</span><span class="sxs-lookup"><span data-stu-id="07e2e-189">**RefPicSetStCurrAfter**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="07e2e-190">**Ref-setltcurrr**</span><span class="sxs-lookup"><span data-stu-id="07e2e-190">**RefPicSetLtCurr**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="07e2e-191">**ReservedBits6**</span><span class="sxs-lookup"><span data-stu-id="07e2e-191">**ReservedBits6**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="07e2e-192">**ReservedBits7**</span><span class="sxs-lookup"><span data-stu-id="07e2e-192">**ReservedBits7**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="07e2e-193">**Status Report feedbacknumber**</span><span class="sxs-lookup"><span data-stu-id="07e2e-193">**StatusReportFeedbackNumber**</span></span>
<span data-ttu-id="07e2e-194"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="07e2e-194"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="07e2e-195">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="07e2e-195">Requirements</span></span>



| <span data-ttu-id="07e2e-196">Anforderung</span><span class="sxs-lookup"><span data-stu-id="07e2e-196">Requirement</span></span> | <span data-ttu-id="07e2e-197">Wert</span><span class="sxs-lookup"><span data-stu-id="07e2e-197">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="07e2e-198">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="07e2e-198">Minimum supported client</span></span><br/> | <span data-ttu-id="07e2e-199">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="07e2e-199">Windows 8.1 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="07e2e-200">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="07e2e-200">Minimum supported server</span></span><br/> | <span data-ttu-id="07e2e-201">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="07e2e-201">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="07e2e-202">Header</span><span class="sxs-lookup"><span data-stu-id="07e2e-202">Header</span></span><br/>                   | <dl> <span data-ttu-id="07e2e-203"><dt>DXVA. h</dt></span><span class="sxs-lookup"><span data-stu-id="07e2e-203"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07e2e-204">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="07e2e-204">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07e2e-205">Media Foundation Strukturen</span><span class="sxs-lookup"><span data-stu-id="07e2e-205">Media Foundation Structures</span></span>](media-foundation-structures.md)
</dt> </dl>

 

 




