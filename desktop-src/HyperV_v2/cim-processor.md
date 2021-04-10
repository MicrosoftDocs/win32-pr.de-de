---
description: Stellt die Funktionen und die Verwaltung eines Prozessors dar.
ms.assetid: 70cf9776-eeda-42c2-90c4-704ecf1cdafe
title: CIM_Processor-Klasse (Hyper-V-Verwaltung)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Processor
- CIM_Processor.Role
- CIM_Processor.Family
- CIM_Processor.OtherFamilyDescription
- CIM_Processor.UpgradeMethod
- CIM_Processor.MaxClockSpeed
- CIM_Processor.CurrentClockSpeed
- CIM_Processor.DataWidth
- CIM_Processor.AddressWidth
- CIM_Processor.LoadPercentage
- CIM_Processor.Stepping
- CIM_Processor.UniqueID
- CIM_Processor.CPUStatus
- CIM_Processor.ExternalBusClockSpeed
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 00e78834c0a3a782c5fdc48cd52a67b85aa2a241
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749641"
---
# <a name="cim_processor-class-hyper-v-management"></a>CIM_Processor-Klasse (Hyper-V-Verwaltung)

Stellt die Funktionen und die Verwaltung eines Prozessors dar.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, Version("2.24.1"), UMLPackagePath("CIM::Device::Processor"), AMENDMENT]
class CIM_Processor : CIM_LogicalDevice
{
  string Role;
  uint16 Family;
  string OtherFamilyDescription;
  uint16 UpgradeMethod;
  uint32 MaxClockSpeed;
  uint32 CurrentClockSpeed;
  uint16 DataWidth;
  uint16 AddressWidth;
  uint16 LoadPercentage;
  string Stepping;
  string UniqueID;
  uint16 CPUStatus;
  uint32 ExternalBusClockSpeed;
};
```

## <a name="members"></a>Member

Die **CIM- \_ Prozessor** Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM- \_ Prozessor** Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Addresswidth**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits"), **Punit** ("Bit")
</dt> </dl>

Die Prozessor Adress Breite in Bits.

</dd> <dt>

**Cpustatus**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der aktuelle Status des Prozessors.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="CPU_Enabled"></span><span id="cpu_enabled"></span><span id="CPU_ENABLED"></span>

**CPU aktiviert** (1)


</dt> <dd></dd> <dt>

<span id="CPU_Disabled_by_User"></span><span id="cpu_disabled_by_user"></span><span id="CPU_DISABLED_BY_USER"></span>

**CPU von Benutzer deaktiviert** (2)


</dt> <dd></dd> <dt>

<span id="CPU_Disabled_By_BIOS__POST_Error_"></span><span id="cpu_disabled_by_bios__post_error_"></span><span id="CPU_DISABLED_BY_BIOS__POST_ERROR_"></span>

**CPU vom BIOS deaktiviert (Post-Fehler)** (3)


</dt> <dd></dd> <dt>

<span id="CPU_Is_Idle"></span><span id="cpu_is_idle"></span><span id="CPU_IS_IDLE"></span>

**CPU befindet sich im Leerlauf** (4)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Sonstige** (7)


</dt> <dd></dd> </dl>

</dd> <dt>

**Weise**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Megahertz"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Prozessor \| 017,6 "), **Punit** (" Hertz \* 10 ^ 6 ")
</dt> </dl>

Die aktuelle Geschwindigkeit des Prozessors in MHz.

</dd> <dt>

**DataWidth**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits"), **Punit** ("Bit")
</dt> </dl>

Die Prozessor Daten Breite in Bits.

</dd> <dt>

**Externalbusclockspeed**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Megahertz"), **Punit** ("Hertz \* 10 ^ 6")
</dt> </dl>

Die Geschwindigkeit der externen Busschnittstelle (auch als Front-Side-Bus bezeichnet) in MHz.

</dd> <dt>

**Familie**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Prozessor \| 017,3 "), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM-**\_ Prozessor**.**Otherfamilydescription**")
</dt> </dl>

Der Typ der Prozessorfamilie.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Sonstige** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (2)


</dt> <dd></dd> <dt>

<span id="8086"></span>

**8086** (3)


</dt> <dd></dd> <dt>

<span id="80286"></span>

**80286** (4)


</dt> <dd></dd> <dt>

<span id="80386"></span>

**80386** (5)


</dt> <dd></dd> <dt>

<span id="80486"></span>

**80486** (6)


</dt> <dd></dd> <dt>

<span id="8087"></span>

**8087** (7)


</dt> <dd></dd> <dt>

<span id="80287"></span>

**80287** (8)


</dt> <dd></dd> <dt>

<span id="80387"></span>

**80387** (9)


</dt> <dd></dd> <dt>

<span id="80487"></span>

**80487** (10)


</dt> <dd></dd> <dt>

<span id="Pentium_R__brand"></span><span id="pentium_r__brand"></span><span id="PENTIUM_R__BRAND"></span>

**Pentium (R)-Marke** (11)


</dt> <dd></dd> <dt>

<span id="Pentium_R__Pro"></span><span id="pentium_r__pro"></span><span id="PENTIUM_R__PRO"></span>

**Pentium (R) pro** (12)


</dt> <dd></dd> <dt>

<span id="Pentium_R__II"></span><span id="pentium_r__ii"></span><span id="PENTIUM_R__II"></span>

**Pentium (R) II** (13)


</dt> <dd></dd> <dt>

<span id="Pentium_R__processor_with_MMX_TM__technology"></span><span id="pentium_r__processor_with_mmx_tm__technology"></span><span id="PENTIUM_R__PROCESSOR_WITH_MMX_TM__TECHNOLOGY"></span>

**Pentium (R)-Prozessor mit MMX (TM)-Technologie** (14)


</dt> <dd></dd> <dt>

<span id="Celeron_TM_"></span><span id="celeron_tm_"></span><span id="CELERON_TM_"></span>

**Celeron (TM)** (15)


</dt> <dd></dd> <dt>

<span id="Pentium_R__II_Xeon_TM_"></span><span id="pentium_r__ii_xeon_tm_"></span><span id="PENTIUM_R__II_XEON_TM_"></span>

**Pentium (R) II Xeon (TM)** (16)


</dt> <dd></dd> <dt>

<span id="Pentium_R__III"></span><span id="pentium_r__iii"></span><span id="PENTIUM_R__III"></span>

**Pentium (R) III** (17)


</dt> <dd></dd> <dt>

<span id="M1_Family"></span><span id="m1_family"></span><span id="M1_FAMILY"></span>

**M1-Familie** (18)


</dt> <dd></dd> <dt>

<span id="M2_Family"></span><span id="m2_family"></span><span id="M2_FAMILY"></span>

**M2-Familie** (19)


</dt> <dd></dd> <dt>

<span id="Intel_R__Celeron_R__M_processor"></span><span id="intel_r__celeron_r__m_processor"></span><span id="INTEL_R__CELERON_R__M_PROCESSOR"></span>

**Intel (r) Celeron (r) M Prozessor** (20)


</dt> <dd></dd> <dt>

<span id="Intel_R__Pentium_R__4_HT_processor"></span><span id="intel_r__pentium_r__4_ht_processor"></span><span id="INTEL_R__PENTIUM_R__4_HT_PROCESSOR"></span>

**Intel (r) Pentium (r) 4 HT-Prozessor** (21)


</dt> <dd></dd> <dt>

<span id="K5_Family"></span><span id="k5_family"></span><span id="K5_FAMILY"></span>

**K5-Familie** (24)


</dt> <dd></dd> <dt>

<span id="K6_Family"></span><span id="k6_family"></span><span id="K6_FAMILY"></span>

**K6-Familie** (25)


</dt> <dd></dd> <dt>

<span id="K6-2"></span><span id="k6-2"></span>

**K6-2** (26)


</dt> <dd></dd> <dt>

<span id="K6-3"></span><span id="k6-3"></span>

**K6-3** (27)


</dt> <dd></dd> <dt>

<span id="AMD_Athlon_TM__Processor_Family"></span><span id="amd_athlon_tm__processor_family"></span><span id="AMD_ATHLON_TM__PROCESSOR_FAMILY"></span>

**AMD Athlon (TM)-Prozessorfamilie** (28)


</dt> <dd></dd> <dt>

<span id="AMD_R__Duron_TM__Processor"></span><span id="amd_r__duron_tm__processor"></span><span id="AMD_R__DURON_TM__PROCESSOR"></span>

**AMD (R) Duron (TM)-Prozessor** (29)


</dt> <dd></dd> <dt>

<span id="AMD29000_Family"></span><span id="amd29000_family"></span><span id="AMD29000_FAMILY"></span>

**AMD29000-Familie** (30)


</dt> <dd></dd> <dt>

<span id="K6-2_"></span><span id="k6-2_"></span>

**K6-2 +** (31)


</dt> <dd></dd> <dt>

<span id="Power_PC_Family"></span><span id="power_pc_family"></span><span id="POWER_PC_FAMILY"></span>

**Power PC-Familie** (32)


</dt> <dd></dd> <dt>

<span id="Power_PC_601"></span><span id="power_pc_601"></span><span id="POWER_PC_601"></span>

**Power PC 601** (33)


</dt> <dd></dd> <dt>

<span id="Power_PC_603"></span><span id="power_pc_603"></span><span id="POWER_PC_603"></span>

**Power PC 603** (34)


</dt> <dd></dd> <dt>

<span id="Power_PC_603_"></span><span id="power_pc_603_"></span><span id="POWER_PC_603_"></span>

**Power PC 603** und höher (35)


</dt> <dd></dd> <dt>

<span id="Power_PC_604"></span><span id="power_pc_604"></span><span id="POWER_PC_604"></span>

**Power PC 604** (36)


</dt> <dd></dd> <dt>

<span id="Power_PC_620"></span><span id="power_pc_620"></span><span id="POWER_PC_620"></span>

**Power PC 620** (37)


</dt> <dd></dd> <dt>

<span id="Power_PC_X704"></span><span id="power_pc_x704"></span><span id="POWER_PC_X704"></span>

**Power PC-X704** (38)


</dt> <dd></dd> <dt>

<span id="Power_PC_750"></span><span id="power_pc_750"></span><span id="POWER_PC_750"></span>

**Power PC 750** (39)


</dt> <dd></dd> <dt>

<span id="Intel_R__Core_TM__Duo_processor"></span><span id="intel_r__core_tm__duo_processor"></span><span id="INTEL_R__CORE_TM__DUO_PROCESSOR"></span>

**Intel (R) Core (TM)-Duo-Prozessor** (40)


</dt> <dd></dd> <dt>

<span id="Intel_R__Core_TM__Duo_mobile_processor"></span><span id="intel_r__core_tm__duo_mobile_processor"></span><span id="INTEL_R__CORE_TM__DUO_MOBILE_PROCESSOR"></span>

**Intel (R) Core (TM)-Duo (mobiler Prozessor** ) (41)


</dt> <dd></dd> <dt>

<span id="Intel_R__Core_TM__Solo_mobile_processor"></span><span id="intel_r__core_tm__solo_mobile_processor"></span><span id="INTEL_R__CORE_TM__SOLO_MOBILE_PROCESSOR"></span>

**Intel (R) Core (TM)-Einzel Mobil Prozessor** (42)


</dt> <dd></dd> <dt>

<span id="Intel_R__Atom_TM__processor"></span><span id="intel_r__atom_tm__processor"></span><span id="INTEL_R__ATOM_TM__PROCESSOR"></span>

**Intel (R) Atom (TM)-Prozessor** (43)


</dt> <dd></dd> <dt>

<span id="Alpha_Family"></span><span id="alpha_family"></span><span id="ALPHA_FAMILY"></span>

**Alpha-Familie** (48)


</dt> <dd></dd> <dt>

<span id="Alpha_21064"></span><span id="alpha_21064"></span><span id="ALPHA_21064"></span>

**Alpha 21064** (49)


</dt> <dd></dd> <dt>

<span id="Alpha_21066"></span><span id="alpha_21066"></span><span id="ALPHA_21066"></span>

**Alpha 21066** (50)


</dt> <dd></dd> <dt>

<span id="Alpha_21164"></span><span id="alpha_21164"></span><span id="ALPHA_21164"></span>

**Alpha 21164** (51)


</dt> <dd></dd> <dt>

<span id="Alpha_21164PC"></span><span id="alpha_21164pc"></span><span id="ALPHA_21164PC"></span>

**Alpha 21164pc** (52)


</dt> <dd></dd> <dt>

<span id="Alpha_21164a"></span><span id="alpha_21164a"></span><span id="ALPHA_21164A"></span>

**Alpha 21164A** (53)


</dt> <dd></dd> <dt>

<span id="Alpha_21264"></span><span id="alpha_21264"></span><span id="ALPHA_21264"></span>

**Alpha 21264** (54)


</dt> <dd></dd> <dt>

<span id="Alpha_21364"></span><span id="alpha_21364"></span><span id="ALPHA_21364"></span>

**Alpha 21364** (55)


</dt> <dd></dd> <dt>

<span id="AMD_Turion_TM__II_Ultra_Dual-Core_Mobile_M_Processor_Family"></span><span id="amd_turion_tm__ii_ultra_dual-core_mobile_m_processor_family"></span><span id="AMD_TURION_TM__II_ULTRA_DUAL-CORE_MOBILE_M_PROCESSOR_FAMILY"></span>

**AMD Turion (TM) II Ultra Dual-Core Mobile M-Prozessorfamilie** (56)


</dt> <dd></dd> <dt>

<span id="AMD_Turion_TM__II_Dual-Core_Mobile_M_Processor_Family"></span><span id="amd_turion_tm__ii_dual-core_mobile_m_processor_family"></span><span id="AMD_TURION_TM__II_DUAL-CORE_MOBILE_M_PROCESSOR_FAMILY"></span>

**AMD Turion (TM) II Dual-Core Mobile M-Prozessorfamilie** (57)


</dt> <dd></dd> <dt>

<span id="AMD_Athlon_TM__II_Dual-Core_Mobile_M_Processor_Family"></span><span id="amd_athlon_tm__ii_dual-core_mobile_m_processor_family"></span><span id="AMD_ATHLON_TM__II_DUAL-CORE_MOBILE_M_PROCESSOR_FAMILY"></span>

**AMD Athlon (TM) II Dual-Core Mobile M-Prozessorfamilie** (58)


</dt> <dd></dd> <dt>

<span id="AMD_Opteron_TM__6100_Series_Processor"></span><span id="amd_opteron_tm__6100_series_processor"></span><span id="AMD_OPTERON_TM__6100_SERIES_PROCESSOR"></span>

**AMD Opteron (TM) 6100-Serie** (59)


</dt> <dd></dd> <dt>

<span id="AMD_Opteron_TM__4100_Series_Processor"></span><span id="amd_opteron_tm__4100_series_processor"></span><span id="AMD_OPTERON_TM__4100_SERIES_PROCESSOR"></span>

**AMD Opteron (TM) 4100-Serie** (60)


</dt> <dd></dd> <dt>

<span id="MIPS_Family"></span><span id="mips_family"></span><span id="MIPS_FAMILY"></span>

**MIPS-Familie** (64)


</dt> <dd></dd> <dt>

<span id="MIPS_R4000"></span><span id="mips_r4000"></span>

**MIPS R4000** (65)


</dt> <dd></dd> <dt>

<span id="MIPS_R4200"></span><span id="mips_r4200"></span>

**MIPS r4200 optimieren** (66)


</dt> <dd></dd> <dt>

<span id="MIPS_R4400"></span><span id="mips_r4400"></span>

**MIPS R4400** (67)


</dt> <dd></dd> <dt>

<span id="MIPS_R4600"></span><span id="mips_r4600"></span>

**MIPS R4600** (68)


</dt> <dd></dd> <dt>

<span id="MIPS_R10000"></span><span id="mips_r10000"></span>

**MIPS R10000** (69)


</dt> <dd></dd> <dt>

<span id="SPARC_Family"></span><span id="sparc_family"></span><span id="SPARC_FAMILY"></span>

**SPARC-Familie** (80)


</dt> <dd></dd> <dt>

<span id="SuperSPARC"></span><span id="supersparc"></span><span id="SUPERSPARC"></span>

**SuperSPARC** (81)


</dt> <dd></dd> <dt>

<span id="microSPARC_II"></span><span id="microsparc_ii"></span><span id="MICROSPARC_II"></span>

**mikrosparc II** (82)


</dt> <dd></dd> <dt>

<span id="microSPARC_IIep"></span><span id="microsparc_iiep"></span><span id="MICROSPARC_IIEP"></span>

**mikrosparc-iiep** (83)


</dt> <dd></dd> <dt>

<span id="UltraSPARC"></span><span id="ultrasparc"></span><span id="ULTRASPARC"></span>

**UltraSPARC** (84)


</dt> <dd></dd> <dt>

<span id="UltraSPARC_II"></span><span id="ultrasparc_ii"></span><span id="ULTRASPARC_II"></span>

**UltraSPARC II** (85)


</dt> <dd></dd> <dt>

<span id="UltraSPARC_IIi"></span><span id="ultrasparc_iii"></span><span id="ULTRASPARC_III"></span>

**UltraSPARC III** (86)


</dt> <dd></dd> <dt>

<span id="UltraSPARC_III"></span><span id="ultrasparc_iii"></span><span id="ULTRASPARC_III"></span>

**UltraSPARC III** (87)


</dt> <dd></dd> <dt>

<span id="UltraSPARC_IIIi"></span><span id="ultrasparc_iiii"></span><span id="ULTRASPARC_IIII"></span>

**UltraSPARC IIII** (88)


</dt> <dd></dd> <dt>

<span id="68040"></span>

**68040** (96)


</dt> <dd></dd> <dt>

<span id="68xxx_Family"></span><span id="68xxx_family"></span><span id="68XXX_FAMILY"></span>

**68xxx-Familie** (97)


</dt> <dd></dd> <dt>

<span id="68000"></span>

**68000** (98)


</dt> <dd></dd> <dt>

<span id="68010"></span>

**68010** (99)


</dt> <dd></dd> <dt>

<span id="68020"></span>

**68020** (100)


</dt> <dd></dd> <dt>

<span id="68030"></span>

**68030** (101)


</dt> <dd></dd> <dt>

<span id="Hobbit_Family"></span><span id="hobbit_family"></span><span id="HOBBIT_FAMILY"></span>

**Hobbit-Familie** (112)


</dt> <dd></dd> <dt>

<span id="Crusoe_TM__TM5000_Family"></span><span id="crusoe_tm__tm5000_family"></span><span id="CRUSOE_TM__TM5000_FAMILY"></span>

**Crusoe (TM) TM5000-Familie** (120)


</dt> <dd></dd> <dt>

<span id="Crusoe_TM__TM3000_Family"></span><span id="crusoe_tm__tm3000_family"></span><span id="CRUSOE_TM__TM3000_FAMILY"></span>

**Crusoe (TM) TM3000-Familie** (121)


</dt> <dd></dd> <dt>

<span id="Efficeon_TM__TM8000_Family"></span><span id="efficeon_tm__tm8000_family"></span><span id="EFFICEON_TM__TM8000_FAMILY"></span>

**Efficeon (TM) TM8000 Familie** (122)


</dt> <dd></dd> <dt>

<span id="Weitek"></span><span id="weitek"></span><span id="WEITEK"></span>

**Weitek** (128)


</dt> <dd></dd> <dt>

<span id="Itanium_TM__Processor"></span><span id="itanium_tm__processor"></span><span id="ITANIUM_TM__PROCESSOR"></span>

**Itanium (TM)-Prozessor** (130)


</dt> <dd></dd> <dt>

<span id="AMD_Athlon_TM__64_Processor_Family"></span><span id="amd_athlon_tm__64_processor_family"></span><span id="AMD_ATHLON_TM__64_PROCESSOR_FAMILY"></span>

**AMD Athlon (TM) 64-Prozessorfamilie** (131)


</dt> <dd></dd> <dt>

<span id="AMD_Opteron_TM__Processor_Family"></span><span id="amd_opteron_tm__processor_family"></span><span id="AMD_OPTERON_TM__PROCESSOR_FAMILY"></span>

**AMD Opteron (TM)-Prozessorfamilie** (132)


</dt> <dd></dd> <dt>

<span id="AMD_Sempron_TM__Processor_Family"></span><span id="amd_sempron_tm__processor_family"></span><span id="AMD_SEMPRON_TM__PROCESSOR_FAMILY"></span>

**AMD Sempron (TM)-Prozessorfamilie** (133)


</dt> <dd></dd> <dt>

<span id="AMD_Turion_TM__64_Mobile_Technology"></span><span id="amd_turion_tm__64_mobile_technology"></span><span id="AMD_TURION_TM__64_MOBILE_TECHNOLOGY"></span>

**AMD Turion (TM) 64 Mobile-Technologie** (134)


</dt> <dd></dd> <dt>

<span id="Dual-Core_AMD_Opteron_TM__Processor_Family"></span><span id="dual-core_amd_opteron_tm__processor_family"></span><span id="DUAL-CORE_AMD_OPTERON_TM__PROCESSOR_FAMILY"></span>

**Dual-Core AMD Opteron (TM)-Prozessorfamilie** (135)


</dt> <dd></dd> <dt>

<span id="AMD_Athlon_TM__64_X2_Dual-Core_Processor_Family"></span><span id="amd_athlon_tm__64_x2_dual-core_processor_family"></span><span id="AMD_ATHLON_TM__64_X2_DUAL-CORE_PROCESSOR_FAMILY"></span>

**AMD Athlon (TM) 64 x2 Dual-Core Prozessorfamilie** (136)


</dt> <dd></dd> <dt>

<span id="AMD_Turion_TM__64_X2_Mobile_Technology"></span><span id="amd_turion_tm__64_x2_mobile_technology"></span><span id="AMD_TURION_TM__64_X2_MOBILE_TECHNOLOGY"></span>

**AMD Turion (TM) 64 x2 Mobile Technology** (137)


</dt> <dd></dd> <dt>

<span id="Quad-Core_AMD_Opteron_TM__Processor_Family"></span><span id="quad-core_amd_opteron_tm__processor_family"></span><span id="QUAD-CORE_AMD_OPTERON_TM__PROCESSOR_FAMILY"></span>

**Quad-Core AMD Opteron (TM)-Prozessorfamilie** (138)


</dt> <dd></dd> <dt>

<span id="Third-Generation_AMD_Opteron_TM__Processor_Family"></span><span id="third-generation_amd_opteron_tm__processor_family"></span><span id="THIRD-GENERATION_AMD_OPTERON_TM__PROCESSOR_FAMILY"></span>

**AMD Opteron (TM)-Prozessorfamilie der dritten Generation** (139)


</dt> <dd></dd> <dt>

<span id="AMD_Phenom_TM__FX_Quad-Core_Processor_Family"></span><span id="amd_phenom_tm__fx_quad-core_processor_family"></span><span id="AMD_PHENOM_TM__FX_QUAD-CORE_PROCESSOR_FAMILY"></span>

**AMD Phenom (TM) FX Quad-Core-Prozessorfamilie** (140)


</dt> <dd></dd> <dt>

<span id="AMD_Phenom_TM__X4_Quad-Core_Processor_Family"></span><span id="amd_phenom_tm__x4_quad-core_processor_family"></span><span id="AMD_PHENOM_TM__X4_QUAD-CORE_PROCESSOR_FAMILY"></span>

**AMD Phenom (TM) X4 Quad-Core Prozessorfamilie** (141)


</dt> <dd></dd> <dt>

<span id="AMD_Phenom_TM__X2_Dual-Core_Processor_Family"></span><span id="amd_phenom_tm__x2_dual-core_processor_family"></span><span id="AMD_PHENOM_TM__X2_DUAL-CORE_PROCESSOR_FAMILY"></span>

**AMD Phenom (TM) x2 Dual-Core Prozessorfamilie** (142)


</dt> <dd></dd> <dt>

<span id="AMD_Athlon_TM__X2_Dual-Core_Processor_Family"></span><span id="amd_athlon_tm__x2_dual-core_processor_family"></span><span id="AMD_ATHLON_TM__X2_DUAL-CORE_PROCESSOR_FAMILY"></span>

**AMD Athlon (TM) x2 Dual-Core Prozessorfamilie** (143)


</dt> <dd></dd> <dt>

<span id="PA-RISC_Family"></span><span id="pa-risc_family"></span><span id="PA-RISC_FAMILY"></span>

**PA-RISC-Familie** (144)


</dt> <dd></dd> <dt>

<span id="PA-RISC_8500"></span><span id="pa-risc_8500"></span>

**PA-RISC 8500** (145)


</dt> <dd></dd> <dt>

<span id="PA-RISC_8000"></span><span id="pa-risc_8000"></span>

**PA-RISC 8000** (146)


</dt> <dd></dd> <dt>

<span id="PA-RISC_7300LC"></span><span id="pa-risc_7300lc"></span>

**PA-RISC 7300LC** (147)


</dt> <dd></dd> <dt>

<span id="PA-RISC_7200"></span><span id="pa-risc_7200"></span>

**PA-RISC 7200** (148)


</dt> <dd></dd> <dt>

<span id="PA-RISC_7100LC"></span><span id="pa-risc_7100lc"></span>

**PA-RISC 7100LC** (149)


</dt> <dd></dd> <dt>

<span id="PA-RISC_7100"></span><span id="pa-risc_7100"></span>

**PA-RISC 7100** (150)


</dt> <dd></dd> <dt>

<span id="V30_Family"></span><span id="v30_family"></span><span id="V30_FAMILY"></span>

**V30-Familie** (160)


</dt> <dd></dd> <dt>

<span id="Quad-Core_Intel_R__Xeon_R__processor_3200_Series"></span><span id="quad-core_intel_r__xeon_r__processor_3200_series"></span><span id="QUAD-CORE_INTEL_R__XEON_R__PROCESSOR_3200_SERIES"></span>

**Vierkern-Intel (r) Xeon (r) Prozessor 3200-Serie** (161)


</dt> <dd></dd> <dt>

<span id="Dual-Core_Intel_R__Xeon_R__processor_3000_Series"></span><span id="dual-core_intel_r__xeon_r__processor_3000_series"></span><span id="DUAL-CORE_INTEL_R__XEON_R__PROCESSOR_3000_SERIES"></span>

**Dual-Core Intel (r) Xeon (r) Prozessor 3000-Serie** (162)


</dt> <dd></dd> <dt>

<span id="Quad-Core_Intel_R__Xeon_R__processor_5300_Series"></span><span id="quad-core_intel_r__xeon_r__processor_5300_series"></span><span id="QUAD-CORE_INTEL_R__XEON_R__PROCESSOR_5300_SERIES"></span>

**Vierkern-Intel (r) Xeon (r) Prozessor 5300-Serie** (163)


</dt> <dd></dd> <dt>

<span id="Dual-Core_Intel_R__Xeon_R__processor_5100_Series"></span><span id="dual-core_intel_r__xeon_r__processor_5100_series"></span><span id="DUAL-CORE_INTEL_R__XEON_R__PROCESSOR_5100_SERIES"></span>

**Dual-Core Intel (r) Xeon (r) Prozessor 5100-Serie** (164)


</dt> <dd></dd> <dt>

<span id="Dual-Core_Intel_R__Xeon_R__processor_5000_Series"></span><span id="dual-core_intel_r__xeon_r__processor_5000_series"></span><span id="DUAL-CORE_INTEL_R__XEON_R__PROCESSOR_5000_SERIES"></span>

**Dual-Core Intel (r) Xeon (r) Prozessor 5000-Serie** (165)


</dt> <dd></dd> <dt>

<span id="Dual-Core_Intel_R__Xeon_R__processor_LV"></span><span id="dual-core_intel_r__xeon_r__processor_lv"></span><span id="DUAL-CORE_INTEL_R__XEON_R__PROCESSOR_LV"></span>

**Dual-Core Intel (r) Xeon (r) Processor LV** (166)


</dt> <dd></dd> <dt>

<span id="Dual-Core_Intel_R__Xeon_R__processor_ULV"></span><span id="dual-core_intel_r__xeon_r__processor_ulv"></span><span id="DUAL-CORE_INTEL_R__XEON_R__PROCESSOR_ULV"></span>

**Dual-Core Intel (r) Xeon (r) Processor ULV** (167)


</dt> <dd></dd> <dt>

<span id="Dual-Core_Intel_R__Xeon_R__processor_7100_Series"></span><span id="dual-core_intel_r__xeon_r__processor_7100_series"></span><span id="DUAL-CORE_INTEL_R__XEON_R__PROCESSOR_7100_SERIES"></span>

**Dual-Core Intel (r) Xeon (r) Prozessor 7100-Serie** (168)


</dt> <dd></dd> <dt>

<span id="Quad-Core_Intel_R__Xeon_R__processor_5400_Series"></span><span id="quad-core_intel_r__xeon_r__processor_5400_series"></span><span id="QUAD-CORE_INTEL_R__XEON_R__PROCESSOR_5400_SERIES"></span>

**Vierkern-Intel (r) Xeon (r) Prozessor 5400-Serie** (169)


</dt> <dd></dd> <dt>

<span id="Quad-Core_Intel_R__Xeon_R__processor"></span><span id="quad-core_intel_r__xeon_r__processor"></span><span id="QUAD-CORE_INTEL_R__XEON_R__PROCESSOR"></span>

**Vierkern-Intel (r) Xeon (r)-Prozessor** (170)


</dt> <dd></dd> <dt>

<span id="Dual-Core_Intel_R__Xeon_R__processor_5200_Series"></span><span id="dual-core_intel_r__xeon_r__processor_5200_series"></span><span id="DUAL-CORE_INTEL_R__XEON_R__PROCESSOR_5200_SERIES"></span>

**Dual-Core Intel (r) Xeon (r) Prozessor 5200-Serie** (171)


</dt> <dd></dd> <dt>

<span id="Dual-Core_Intel_R__Xeon_R__processor_7200_Series"></span><span id="dual-core_intel_r__xeon_r__processor_7200_series"></span><span id="DUAL-CORE_INTEL_R__XEON_R__PROCESSOR_7200_SERIES"></span>

**Dual-Core Intel (r) Xeon (r) Prozessor 7200-Serie** (172)


</dt> <dd></dd> <dt>

<span id="Quad-Core_Intel_R__Xeon_R__processor_7300_Series"></span><span id="quad-core_intel_r__xeon_r__processor_7300_series"></span><span id="QUAD-CORE_INTEL_R__XEON_R__PROCESSOR_7300_SERIES"></span>

**Vierkern-Intel (r) Xeon (r) Prozessor 7300-Serie** (173)


</dt> <dd></dd> <dt>

<span id="Quad-Core_Intel_R__Xeon_R__processor_7400_Series"></span><span id="quad-core_intel_r__xeon_r__processor_7400_series"></span><span id="QUAD-CORE_INTEL_R__XEON_R__PROCESSOR_7400_SERIES"></span>

**Vierkern-Intel (r) Xeon (r) Prozessor 7400-Serie** (174)


</dt> <dd></dd> <dt>

<span id="Multi-Core_Intel_R__Xeon_R__processor_7400_Series"></span><span id="multi-core_intel_r__xeon_r__processor_7400_series"></span><span id="MULTI-CORE_INTEL_R__XEON_R__PROCESSOR_7400_SERIES"></span>

**Mehr Kern-Intel (r) Xeon (r) Prozessor 7400-Serie** (175)


</dt> <dd></dd> <dt>

<span id="Pentium_R__III_Xeon_TM_"></span><span id="pentium_r__iii_xeon_tm_"></span><span id="PENTIUM_R__III_XEON_TM_"></span>

**Pentium (R) III Xeon (TM)** (176)


</dt> <dd></dd> <dt>

<span id="Pentium_R__III_Processor_with_Intel_R__SpeedStep_TM__Technology"></span><span id="pentium_r__iii_processor_with_intel_r__speedstep_tm__technology"></span><span id="PENTIUM_R__III_PROCESSOR_WITH_INTEL_R__SPEEDSTEP_TM__TECHNOLOGY"></span>

**Pentium (r) III-Prozessor mit Intel (r) SpeedStep (TM)-Technologie** (177)


</dt> <dd></dd> <dt>

<span id="Pentium_R__4"></span><span id="pentium_r__4"></span><span id="PENTIUM_R__4"></span>

**Pentium (R) 4** (178)


</dt> <dd></dd> <dt>

<span id="Intel_R__Xeon_TM_"></span><span id="intel_r__xeon_tm_"></span><span id="INTEL_R__XEON_TM_"></span>

**Intel (R) Xeon (TM)** (179)


</dt> <dd></dd> <dt>

<span id="AS400_Family"></span><span id="as400_family"></span><span id="AS400_FAMILY"></span>

**AS400-Familie** (180)


</dt> <dd></dd> <dt>

<span id="Intel_R__Xeon_TM__processor_MP"></span><span id="intel_r__xeon_tm__processor_mp"></span><span id="INTEL_R__XEON_TM__PROCESSOR_MP"></span>

**Intel (R) Xeon (TM)-Prozessor-MP** (181)


</dt> <dd></dd> <dt>

<span id="AMD_Athlon_TM__XP_Family"></span><span id="amd_athlon_tm__xp_family"></span><span id="AMD_ATHLON_TM__XP_FAMILY"></span>

**AMD Athlon (TM) XP-Familie** (182)


</dt> <dd></dd> <dt>

<span id="AMD_Athlon_TM__MP_Family"></span><span id="amd_athlon_tm__mp_family"></span><span id="AMD_ATHLON_TM__MP_FAMILY"></span>

**AMD Athlon (TM) MP-Familie** (183)


</dt> <dd></dd> <dt>

<span id="Intel_R__Itanium_R__2"></span><span id="intel_r__itanium_r__2"></span><span id="INTEL_R__ITANIUM_R__2"></span>

**Intel (r) Itanium (r) 2** (184)


</dt> <dd></dd> <dt>

<span id="Intel_R__Pentium_R__M_processor"></span><span id="intel_r__pentium_r__m_processor"></span><span id="INTEL_R__PENTIUM_R__M_PROCESSOR"></span>

**Intel (r) Pentium (r) M-Prozessor** (185)


</dt> <dd></dd> <dt>

<span id="Intel_R__Celeron_R__D_processor"></span><span id="intel_r__celeron_r__d_processor"></span><span id="INTEL_R__CELERON_R__D_PROCESSOR"></span>

**Intel (r) Celeron (r) D-Prozessor** (186)


</dt> <dd></dd> <dt>

<span id="Intel_R__Pentium_R__D_processor"></span><span id="intel_r__pentium_r__d_processor"></span><span id="INTEL_R__PENTIUM_R__D_PROCESSOR"></span>

**Intel (r) Pentium (r) D-Prozessor** (187)


</dt> <dd></dd> <dt>

<span id="Intel_R__Pentium_R__Processor_Extreme_Edition"></span><span id="intel_r__pentium_r__processor_extreme_edition"></span><span id="INTEL_R__PENTIUM_R__PROCESSOR_EXTREME_EDITION"></span>

**Intel (r) Pentium (r) Processor Extreme Edition** (188)


</dt> <dd></dd> <dt>

<span id="Intel_R__Core_TM__Solo_Processor"></span><span id="intel_r__core_tm__solo_processor"></span><span id="INTEL_R__CORE_TM__SOLO_PROCESSOR"></span>

**Intel (R) Core (TM)-Einzel Prozessor** (189)


</dt> <dd></dd> <dt>

<span id="K7"></span><span id="k7"></span>

**K7** (190)


</dt> <dd></dd> <dt>

<span id="Intel_R__Core_TM_2_Duo_Processor"></span><span id="intel_r__core_tm_2_duo_processor"></span><span id="INTEL_R__CORE_TM_2_DUO_PROCESSOR"></span>

**Intel (R) Core (TM) 2-Duo-Prozessor** (191)


</dt> <dd></dd> <dt>

<span id="Intel_R__Core_TM_2_Solo_processor"></span><span id="intel_r__core_tm_2_solo_processor"></span><span id="INTEL_R__CORE_TM_2_SOLO_PROCESSOR"></span>

**Intel (R) Core (TM) 2-Einzel Prozessor** (192)


</dt> <dd></dd> <dt>

<span id="Intel_R__Core_TM_2_Extreme_processor"></span><span id="intel_r__core_tm_2_extreme_processor"></span><span id="INTEL_R__CORE_TM_2_EXTREME_PROCESSOR"></span>

**Intel (R) Core (TM) 2 Extreme Processor** (193)


</dt> <dd></dd> <dt>

<span id="Intel_R__Core_TM_2_Quad_processor"></span><span id="intel_r__core_tm_2_quad_processor"></span><span id="INTEL_R__CORE_TM_2_QUAD_PROCESSOR"></span>

**Intel (R) Core (TM) 2 Quad-Prozessor** (194)


</dt> <dd></dd> <dt>

<span id="Intel_R__Core_TM_2_Extreme_mobile_processor"></span><span id="intel_r__core_tm_2_extreme_mobile_processor"></span><span id="INTEL_R__CORE_TM_2_EXTREME_MOBILE_PROCESSOR"></span>

**Intel (R) Core (TM) 2 extrem mobiler Prozessor** (195)


</dt> <dd></dd> <dt>

<span id="Intel_R__Core_TM_2_Duo_mobile_processor"></span><span id="intel_r__core_tm_2_duo_mobile_processor"></span><span id="INTEL_R__CORE_TM_2_DUO_MOBILE_PROCESSOR"></span>

**Intel (R) Core (TM) 2 Duo Mobile Processor** (196)


</dt> <dd></dd> <dt>

<span id="Intel_R__Core_TM_2_Solo_mobile_processor"></span><span id="intel_r__core_tm_2_solo_mobile_processor"></span><span id="INTEL_R__CORE_TM_2_SOLO_MOBILE_PROCESSOR"></span>

**Intel (R) Core (TM) 2-Einzel Mobil Prozessor** (197)


</dt> <dd></dd> <dt>

<span id="Intel_R__Core_TM__i7_processor"></span><span id="intel_r__core_tm__i7_processor"></span><span id="INTEL_R__CORE_TM__I7_PROCESSOR"></span>

**Intel (R) Core (TM)-i7-Prozessor** (198)


</dt> <dd></dd> <dt>

<span id="Dual-Core_Intel_R__Celeron_R__Processor"></span><span id="dual-core_intel_r__celeron_r__processor"></span><span id="DUAL-CORE_INTEL_R__CELERON_R__PROCESSOR"></span>

**Dual-Core Intel (r) Celeron (r)-Prozessor** (199)


</dt> <dd></dd> <dt>

<span id="S_390_and_zSeries_Family"></span><span id="s_390_and_zseries_family"></span><span id="S_390_AND_ZSERIES_FAMILY"></span>

**S/390 und zSeries-Familie** (200)


</dt> <dd></dd> <dt>

<span id="ESA_390_G4"></span><span id="esa_390_g4"></span>

**ESA/390 G4** (201)


</dt> <dd></dd> <dt>

<span id="ESA_390_G5"></span><span id="esa_390_g5"></span>

**ESA/390 G5** (202)


</dt> <dd></dd> <dt>

<span id="ESA_390_G6"></span><span id="esa_390_g6"></span>

**ESA/390 G6** (203)


</dt> <dd></dd> <dt>

<span id="z_Architectur_base"></span><span id="z_architectur_base"></span><span id="Z_ARCHITECTUR_BASE"></span>

**Basis für z/Architecture** (204)


</dt> <dd></dd> <dt>

<span id="Intel_R__Core_TM__i5_processor"></span><span id="intel_r__core_tm__i5_processor"></span><span id="INTEL_R__CORE_TM__I5_PROCESSOR"></span>

**Intel (R) Core (TM) i5-Prozessor** (205)


</dt> <dd></dd> <dt>

<span id="Intel_R__Core_TM__i3_processor"></span><span id="intel_r__core_tm__i3_processor"></span><span id="INTEL_R__CORE_TM__I3_PROCESSOR"></span>

**Intel (R) Core (TM) I3-Prozessor** (206)


</dt> <dd></dd> <dt>

<span id="VIA_C7_TM_-M_Processor_Family"></span><span id="via_c7_tm_-m_processor_family"></span><span id="VIA_C7_TM_-M_PROCESSOR_FAMILY"></span>

**Via C7 (TM)-M Prozessorfamilie** (210)


</dt> <dd></dd> <dt>

<span id="VIA_C7_TM_-D_Processor_Family"></span><span id="via_c7_tm_-d_processor_family"></span><span id="VIA_C7_TM_-D_PROCESSOR_FAMILY"></span>

**Via C7 (TM)-D-Prozessorfamilie** (211)


</dt> <dd></dd> <dt>

<span id="VIA_C7_TM__Processor_Family"></span><span id="via_c7_tm__processor_family"></span><span id="VIA_C7_TM__PROCESSOR_FAMILY"></span>

**Via C7 (TM)-Prozessorfamilie** (212)


</dt> <dd></dd> <dt>

<span id="VIA_Eden_TM__Processor_Family"></span><span id="via_eden_tm__processor_family"></span><span id="VIA_EDEN_TM__PROCESSOR_FAMILY"></span>

**Via Eden (TM)-Prozessorfamilie** (213)


</dt> <dd></dd> <dt>

<span id="Multi-Core_Intel_R__Xeon_R__processor"></span><span id="multi-core_intel_r__xeon_r__processor"></span><span id="MULTI-CORE_INTEL_R__XEON_R__PROCESSOR"></span>

**Mehr Kern-Intel (r) Xeon (r)-Prozessor** (214)


</dt> <dd></dd> <dt>

<span id="Dual-Core_Intel_R__Xeon_R__processor_3xxx_Series"></span><span id="dual-core_intel_r__xeon_r__processor_3xxx_series"></span><span id="DUAL-CORE_INTEL_R__XEON_R__PROCESSOR_3XXX_SERIES"></span>

**Dual-Core Intel (r) Xeon (r)-Prozessor 3xxx-Serie** (215)


</dt> <dd></dd> <dt>

<span id="Quad-Core_Intel_R__Xeon_R__processor_3xxx_Series"></span><span id="quad-core_intel_r__xeon_r__processor_3xxx_series"></span><span id="QUAD-CORE_INTEL_R__XEON_R__PROCESSOR_3XXX_SERIES"></span>

**Quad-Core Intel (r) Xeon (r)-Prozessor 3xxx-Serie** (216)


</dt> <dd></dd> <dt>

<span id="VIA_Nano_TM__Processor_Family"></span><span id="via_nano_tm__processor_family"></span><span id="VIA_NANO_TM__PROCESSOR_FAMILY"></span>

**Via Nano (TM)-Prozessorfamilie** (217)


</dt> <dd></dd> <dt>

<span id="Dual-Core_Intel_R__Xeon_R__processor_5xxx_Series"></span><span id="dual-core_intel_r__xeon_r__processor_5xxx_series"></span><span id="DUAL-CORE_INTEL_R__XEON_R__PROCESSOR_5XXX_SERIES"></span>

**Dual-Core Intel (r) Xeon (r) Processor 5xxx Series** (218)


</dt> <dd></dd> <dt>

<span id="Quad-Core_Intel_R__Xeon_R__processor_5xxx_Series"></span><span id="quad-core_intel_r__xeon_r__processor_5xxx_series"></span><span id="QUAD-CORE_INTEL_R__XEON_R__PROCESSOR_5XXX_SERIES"></span>

**Quad-Core Intel (r) Xeon (r) Processor 5xxx Series** (219)


</dt> <dd></dd> <dt>

<span id="Dual-Core_Intel_R__Xeon_R__processor_7xxx_Series"></span><span id="dual-core_intel_r__xeon_r__processor_7xxx_series"></span><span id="DUAL-CORE_INTEL_R__XEON_R__PROCESSOR_7XXX_SERIES"></span>

**Dual-Core Intel (r) Xeon (r)-Prozessor 7xxx-Serie** (221)


</dt> <dd></dd> <dt>

<span id="Quad-Core_Intel_R__Xeon_R__processor_7xxx_Series"></span><span id="quad-core_intel_r__xeon_r__processor_7xxx_series"></span><span id="QUAD-CORE_INTEL_R__XEON_R__PROCESSOR_7XXX_SERIES"></span>

**Vierkern-Intel (r) Xeon (r)-Prozessor 7xxx-Serie** (222)


</dt> <dd></dd> <dt>

<span id="Multi-Core_Intel_R__Xeon_R__processor_7xxx_Series"></span><span id="multi-core_intel_r__xeon_r__processor_7xxx_series"></span><span id="MULTI-CORE_INTEL_R__XEON_R__PROCESSOR_7XXX_SERIES"></span>

**Mehr Kern-Intel (r) Xeon (r)-Prozessor 7xxx-Serie** (223)


</dt> <dd></dd> <dt>

<span id="Multi-Core_Intel_R__Xeon_R__processor_3400_Series"></span><span id="multi-core_intel_r__xeon_r__processor_3400_series"></span><span id="MULTI-CORE_INTEL_R__XEON_R__PROCESSOR_3400_SERIES"></span>

**Mehr Kern-Intel (r) Xeon (r) Prozessor 3400-Serie** (224)


</dt> <dd></dd> <dt>

<span id="Embedded_AMD_Opteron_TM__Quad-Core_Processor_Family"></span><span id="embedded_amd_opteron_tm__quad-core_processor_family"></span><span id="EMBEDDED_AMD_OPTERON_TM__QUAD-CORE_PROCESSOR_FAMILY"></span>

**Eingebettete AMD Opteron (TM) Quad-Core Prozessorfamilie** (230)


</dt> <dd></dd> <dt>

<span id="AMD_Phenom_TM__Triple-Core_Processor_Family"></span><span id="amd_phenom_tm__triple-core_processor_family"></span><span id="AMD_PHENOM_TM__TRIPLE-CORE_PROCESSOR_FAMILY"></span>

**AMD-Phenom (TM) Triple-Core-Prozessorfamilie** (231)


</dt> <dd></dd> <dt>

<span id="AMD_Turion_TM__Ultra_Dual-Core_Mobile_Processor_Family"></span><span id="amd_turion_tm__ultra_dual-core_mobile_processor_family"></span><span id="AMD_TURION_TM__ULTRA_DUAL-CORE_MOBILE_PROCESSOR_FAMILY"></span>

**AMD Turion (TM) Ultra Dual-Core Mobile-Prozessorfamilie** (232)


</dt> <dd></dd> <dt>

<span id="AMD_Turion_TM__Dual-Core_Mobile_Processor_Family"></span><span id="amd_turion_tm__dual-core_mobile_processor_family"></span><span id="AMD_TURION_TM__DUAL-CORE_MOBILE_PROCESSOR_FAMILY"></span>

**AMD Turion (TM) Dual-Core die Mobile Prozessorfamilie** (233)


</dt> <dd></dd> <dt>

<span id="AMD_Athlon_TM__Dual-Core_Processor_Family"></span><span id="amd_athlon_tm__dual-core_processor_family"></span><span id="AMD_ATHLON_TM__DUAL-CORE_PROCESSOR_FAMILY"></span>

**AMD Athlon (TM) Dual-Core Prozessorfamilie** (234)


</dt> <dd></dd> <dt>

<span id="AMD_Sempron_TM__SI_Processor_Family"></span><span id="amd_sempron_tm__si_processor_family"></span><span id="AMD_SEMPRON_TM__SI_PROCESSOR_FAMILY"></span>

**AMD Sempron (TM) Si-Prozessorfamilie** (235)


</dt> <dd></dd> <dt>

<span id="AMD_Phenom_TM__II_Processor_Family"></span><span id="amd_phenom_tm__ii_processor_family"></span><span id="AMD_PHENOM_TM__II_PROCESSOR_FAMILY"></span>

**AMD Phenom (TM) II-Prozessorfamilie** (236)


</dt> <dd></dd> <dt>

<span id="AMD_Athlon_TM__II_Processor_Family"></span><span id="amd_athlon_tm__ii_processor_family"></span><span id="AMD_ATHLON_TM__II_PROCESSOR_FAMILY"></span>

**AMD Athlon (TM) II-Prozessorfamilie** (237)


</dt> <dd></dd> <dt>

<span id="Six-Core_AMD_Opteron_TM__Processor_Family"></span><span id="six-core_amd_opteron_tm__processor_family"></span><span id="SIX-CORE_AMD_OPTERON_TM__PROCESSOR_FAMILY"></span>

**6-Kern-Prozessorfamilie (AMD Opteron) (TM)** (238)


</dt> <dd></dd> <dt>

<span id="AMD_Sempron_TM__M_Processor_Family"></span><span id="amd_sempron_tm__m_processor_family"></span><span id="AMD_SEMPRON_TM__M_PROCESSOR_FAMILY"></span>

**AMD Sempron (TM) M-Prozessorfamilie** (239)


</dt> <dd></dd> <dt>

<span id="i860"></span><span id="I860"></span>

**i860** (250)


</dt> <dd></dd> <dt>

<span id="i960"></span><span id="I960"></span>

**i960** (251)


</dt> <dd></dd> <dt>

<span id="Reserved__SMBIOS_Extension_"></span><span id="reserved__smbios_extension_"></span><span id="RESERVED__SMBIOS_EXTENSION_"></span>

**Reserviert (SMBIOS-Erweiterung)** (254)


</dt> <dd></dd> <dt>

<span id="Reserved__Un-initialized_Flash_Content_-_Lo_"></span><span id="reserved__un-initialized_flash_content_-_lo_"></span><span id="RESERVED__UN-INITIALIZED_FLASH_CONTENT_-_LO_"></span>

**Reserviert (nicht initialisierter Flash Inhalt-Lo)** (255)


</dt> <dd></dd> <dt>

<span id="SH-3"></span><span id="sh-3"></span>

**SH-3** (260)


</dt> <dd></dd> <dt>

<span id="SH-4"></span><span id="sh-4"></span>

**SH-4** (261)


</dt> <dd></dd> <dt>

<span id="ARM"></span><span id="arm"></span>

**Arm** (280)


</dt> <dd></dd> <dt>

<span id="StrongARM"></span><span id="strongarm"></span><span id="STRONGARM"></span>

**StrongARM** (281)


</dt> <dd></dd> <dt>

<span id="6x86"></span><span id="6X86"></span>

**6 x86** (300)


</dt> <dd></dd> <dt>

<span id="MediaGX"></span><span id="mediagx"></span><span id="MEDIAGX"></span>

**MediaGX** (301)


</dt> <dd></dd> <dt>

<span id="MII"></span><span id="mii"></span>

**Mii** (302)


</dt> <dd></dd> <dt>

<span id="WinChip"></span><span id="winchip"></span><span id="WINCHIP"></span>

**WinChip** (320)


</dt> <dd></dd> <dt>

<span id="DSP"></span><span id="dsp"></span>

**DSP** (350)


</dt> <dd></dd> <dt>

<span id="Video_Processor"></span><span id="video_processor"></span><span id="VIDEO_PROCESSOR"></span>

**Video Prozessor** (500)


</dt> <dd></dd> <dt>

<span id="Reserved__For_Future_Special_Purpose_Assignment_"></span><span id="reserved__for_future_special_purpose_assignment_"></span><span id="RESERVED__FOR_FUTURE_SPECIAL_PURPOSE_ASSIGNMENT_"></span>

**Reserviert (für die spätere Zuweisung eines besonderen zwecks)** (65534)


</dt> <dd></dd> <dt>

<span id="Reserved__Un-initialized_Flash_Content_-_Hi_"></span><span id="reserved__un-initialized_flash_content_-_hi_"></span><span id="RESERVED__UN-INITIALIZED_FLASH_CONTENT_-_HI_"></span>

**Reserviert (nicht initialisierter Flash-Inhalt-HI)** (65535)


</dt> <dd></dd> </dl>

</dd> <dt>

**Loadprozentsatz**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Prozent"), [**Messgerät**](/windows/desktop/WmiSdk/standard-qualifiers), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Host-Resources-MIB. hrprocessorload "), **Punit** (" Prozent ")
</dt> </dl>

Das Laden des Prozessors, der in der letzten Minute durchgeführt wurde, als Prozentsatz.

</dd> <dt>

**MaxClockSpeed**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Megahertz"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Prozessor \| 017,5 "), **Punit** (" Hertz \* 10 ^ 6 ")
</dt> </dl>

Die maximale Geschwindigkeit des Prozessors in MHz.

</dd> <dt>

**Otherfamilydescription**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM- \_ Prozessor**.**Familie**")
</dt> </dl>

Der Typ der Prozessorfamilie, wenn die **Family** -Eigenschaft auf " **other** " ("1") festgelegt ist. Diese Zeichenfolge sollte auf NULL festgelegt werden, wenn die Family-Eigenschaft einen anderen Wert als einen **anderen** Wert hat.

</dd> <dt>

**Rolle**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Rolle des Prozessors, z. b. "Central Processor" oder "math Processor".

</dd> <dt>

**Schrittweises Ausführen**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM- \_ Prozessor**".**Familie**")
</dt> </dl>

Die Revisions Ebene des Prozessors innerhalb der Prozessorfamilie.

</dd> <dt>

**UniqueId**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Globally Unique Identifier für den Prozessor innerhalb des Gültigkeits Bereichs der Prozessorfamilie.

</dd> <dt>

**Upgrademethod**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Prozessor \| 017,7 ")
</dt> </dl>

Die CPU-Socketinformationen, die Daten zur Aktualisierung des Prozessors enthalten.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Sonstige** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (2)


</dt> <dd></dd> <dt>

<span id="Daughter_Board"></span><span id="daughter_board"></span><span id="DAUGHTER_BOARD"></span>

**Tochter-Board** (3)


</dt> <dd></dd> <dt>

<span id="ZIF_Socket"></span><span id="zif_socket"></span><span id="ZIF_SOCKET"></span>

**ZIF-Socket** (4)


</dt> <dd></dd> <dt>

<span id="Replacement_Piggy_Back"></span><span id="replacement_piggy_back"></span><span id="REPLACEMENT_PIGGY_BACK"></span>

**Ersetzung/piggy zurück** (5)


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Keine** (6)


</dt> <dd></dd> <dt>

<span id="LIF_Socket"></span><span id="lif_socket"></span><span id="LIF_SOCKET"></span>

**LIF-Socket** (7)


</dt> <dd></dd> <dt>

<span id="Slot_1"></span><span id="slot_1"></span><span id="SLOT_1"></span>

**Slot 1** (8)


</dt> <dd></dd> <dt>

<span id="Slot_2"></span><span id="slot_2"></span><span id="SLOT_2"></span>

**Slot 2** (9)


</dt> <dd></dd> <dt>

<span id="370_Pin_Socket"></span><span id="370_pin_socket"></span><span id="370_PIN_SOCKET"></span>

**370 Pin-Socket** (10)


</dt> <dd></dd> <dt>

<span id="Slot_A"></span><span id="slot_a"></span><span id="SLOT_A"></span>

**Slot A** (11)


</dt> <dd></dd> <dt>

<span id="Slot_M"></span><span id="slot_m"></span><span id="SLOT_M"></span>

**Slot M** (12)


</dt> <dd></dd> <dt>

<span id="Socket_423"></span><span id="socket_423"></span><span id="SOCKET_423"></span>

**Socket 423** (13)


</dt> <dd></dd> <dt>

<span id="Socket_A__Socket_462_"></span><span id="socket_a__socket_462_"></span><span id="SOCKET_A__SOCKET_462_"></span>

**Socket A (Socket 462)** (14)


</dt> <dd></dd> <dt>

<span id="Socket_478"></span><span id="socket_478"></span><span id="SOCKET_478"></span>

**Socket 478** (15)


</dt> <dd></dd> <dt>

<span id="Socket_754"></span><span id="socket_754"></span><span id="SOCKET_754"></span>

**Socket 754** (16)


</dt> <dd></dd> <dt>

<span id="Socket_940"></span><span id="socket_940"></span><span id="SOCKET_940"></span>

**Socket 940** (17)


</dt> <dd></dd> <dt>

<span id="Socket_939"></span><span id="socket_939"></span><span id="SOCKET_939"></span>

**Socket 939** (18)


</dt> <dd></dd> <dt>

<span id="Socket_mPGA604"></span><span id="socket_mpga604"></span><span id="SOCKET_MPGA604"></span>

**Socket mPGA604** (19)


</dt> <dd></dd> <dt>

<span id="Socket_LGA771"></span><span id="socket_lga771"></span><span id="SOCKET_LGA771"></span>

**Socket LGA771** (20)


</dt> <dd></dd> <dt>

<span id="Socket_LGA775"></span><span id="socket_lga775"></span><span id="SOCKET_LGA775"></span>

**Socket LGA775** (21)


</dt> <dd></dd> <dt>

<span id="Socket_S1"></span><span id="socket_s1"></span><span id="SOCKET_S1"></span>

**Socket S1** (22)


</dt> <dd></dd> <dt>

<span id="Socket_AM2"></span><span id="socket_am2"></span><span id="SOCKET_AM2"></span>

**Socket AM2** (23)


</dt> <dd></dd> <dt>

<span id="Socket_F__1207_"></span><span id="socket_f__1207_"></span><span id="SOCKET_F__1207_"></span>

**Socket F (1207)** (24)


</dt> <dd></dd> <dt>

<span id="Socket_LGA1366"></span><span id="socket_lga1366"></span><span id="SOCKET_LGA1366"></span>

**Socket LGA1366** (25)


</dt> <dd></dd> <dt>

<span id="Socket_G34"></span><span id="socket_g34"></span><span id="SOCKET_G34"></span>

**Socket G34** (26)


</dt> <dd></dd> <dt>

<span id="Socket_AM3"></span><span id="socket_am3"></span><span id="SOCKET_AM3"></span>

**Socket AM3** (27)


</dt> <dd></dd> <dt>

<span id="Socket_C32"></span><span id="socket_c32"></span><span id="SOCKET_C32"></span>

**Socket C32** (28)


</dt> <dd></dd> <dt>

<span id="Socket_LGA1156"></span><span id="socket_lga1156"></span><span id="SOCKET_LGA1156"></span>

**Socket LGA1156** (29)


</dt> <dd></dd> <dt>

<span id="Socket_LGA1567"></span><span id="socket_lga1567"></span><span id="SOCKET_LGA1567"></span>

**Socket LGA1567** (30)


</dt> <dd></dd> <dt>

<span id="Socket_PGA988A"></span><span id="socket_pga988a"></span><span id="SOCKET_PGA988A"></span>

**Socket PGA988A** (31)


</dt> <dd></dd> <dt>

<span id="Socket_BGA1288"></span><span id="socket_bga1288"></span><span id="SOCKET_BGA1288"></span>

**Socket-BGA1288** (32)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM \_ LogicalDevice**](cim-logicaldevice.md)
</dt> </dl>

 

