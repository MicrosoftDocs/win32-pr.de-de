---
description: Ein Kommunikationspunkt, der zum Senden und empfangen von Daten zwischen Systemen, Computerschnittstellen und logischen Netzwerken verwendet wird.
ms.assetid: e23ef66b-0bcb-400e-91ff-d6d687d3f0d2
title: CIM_ProtocolEndpoint-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProtocolEndpoint
- CIM_ProtocolEndpoint.Description
- CIM_ProtocolEndpoint.OperationalStatus
- CIM_ProtocolEndpoint.EnabledState
- CIM_ProtocolEndpoint.TimeOfLastStateChange
- CIM_ProtocolEndpoint.Name
- CIM_ProtocolEndpoint.NameFormat
- CIM_ProtocolEndpoint.ProtocolType
- CIM_ProtocolEndpoint.ProtocolIFType
- CIM_ProtocolEndpoint.OtherTypeDescription
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6b3d492c140d443d14583a80985820f55ff9bec8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356176"
---
# <a name="cim_protocolendpoint-class"></a>CIM \_ protocolendpoint-Klasse

Ein Kommunikationspunkt, der zum Senden und empfangen von Daten zwischen Systemen, Computerschnittstellen und logischen Netzwerken verwendet wird.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, Version("2.15.0"), UMLPackagePath("CIM::Core::Service"), AMENDMENT]
class CIM_ProtocolEndpoint : CIM_ServiceAccessPoint
{
  string   Description;
  uint16   OperationalStatus[];
  uint16   EnabledState;
  datetime TimeOfLastStateChange;
  string   Name;
  string   NameFormat;
  uint16   ProtocolType;
  uint16   ProtocolIFType;
  string   OtherTypeDescription;
};
```

## <a name="members"></a>Member

Die **CIM \_ protocolendpoint** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ protocolendpoint** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| if-MIB. ifdescr ")
</dt> </dl>

Eine Textbeschreibung des-Objekts.

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("enabledstate"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| if-MIB. ifadminstatus ")
</dt> </dl>

Der aktivierte Zustand eines Elements.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Name"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Ein eindeutiger Bezeichner des Protokoll Endpunkts, der die verwaltete Funktionalität angibt. Die Benennungs Konvention für diese Eigenschaft wird in der Eigenschaft **NameFormat** definiert.

</dd> <dt>

**NameFormat**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Die Namenskonvention, die von der **Name** -Eigenschaft verwendet wird, um sicherzustellen, dass die **namens** Werte eindeutig sind Beispielsweise können Sie den **protocoliftype** -Eigenschafts Wert an den Anfang des Namens anfügen, gefolgt von einem Unterstrich.

</dd> <dt>

**OperationalStatus**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("OperationalStatus"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| if-MIB. ifOperStatus ")
</dt> </dl>

Ein Array, das den aktuellen Status des Elements enthält. Der erste Wert des **OperationalStatus** -Arrays sollte den primären Status für das Element enthalten.

</dd> <dt>

**OtherTypeDescription**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ protocolendpoint**.**ProtocolType**","**CIM \_ protocolendpoint**.**Protocoliftype**")
</dt> </dl>

Eine Beschreibung eines Netzwerkprotokoll Typs, der verwendet wird, wenn die **protocoliftype** -Eigenschaft auf "1" (sonstige) festgelegt ist. Andernfalls sollte dieser Wert auf NULL festgelegt werden.

</dd> <dt>

**Protocoliftype**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| if-MIB. iftype "), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ protocolendpoint**".**OtherTypeDescription**")
</dt> </dl>

Eine Enumeration, die verwendet wird, um verschiedene Instanzen dieser Klasse zu kategorisieren und zu klassifizieren. Die möglichen Werte für diese Eigenschaft werden mit der Internet Assigned Numbers Authority (IANA) iftype MIB-Module (Verwaltungs Informationsbasis) synchronisiert, das unter verwaltet wird https://www.iana.org/assignments/ianaiftype-mib . Zusätzliche von der DMTF definierte Werte sind enthalten.

> [!Note]  
> Wenn **protocoliftype** auf 1 (Sonstiges) festgelegt ist, sollten die Protokolltyp Informationen in der **OtherTypeDescription** -Eigenschaft bereitgestellt werden.

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Sonstige** (1)


</dt> <dd></dd> <dt>

<span id="Regular_1822"></span><span id="regular_1822"></span><span id="REGULAR_1822"></span>

**Regulär 1822** (2)


</dt> <dd></dd> <dt>

<span id="HDH_1822"></span><span id="hdh_1822"></span>

**HDH 1822** (3)


</dt> <dd></dd> <dt>

<span id="DDN_X.25"></span><span id="ddn_x.25"></span>

**DDN X. 25** (4)


</dt> <dd></dd> <dt>

<span id="RFC877_X.25"></span><span id="rfc877_x.25"></span>

**RFC877 X. 25** (5)


</dt> <dd></dd> <dt>

<span id="Ethernet_CSMA_CD"></span><span id="ethernet_csma_cd"></span><span id="ETHERNET_CSMA_CD"></span>

**Ethernet-CSMA/CD** (6)


</dt> <dd></dd> <dt>

<span id="ISO_802.3_CSMA_CD"></span><span id="iso_802.3_csma_cd"></span>

**ISO 802,3 CSMA/CD** (7)


</dt> <dd></dd> <dt>

<span id="ISO_802.4_Token_Bus"></span><span id="iso_802.4_token_bus"></span><span id="ISO_802.4_TOKEN_BUS"></span>

**ISO 802,4-tokbus** (8)


</dt> <dd></dd> <dt>

<span id="ISO_802.5_Token_Ring"></span><span id="iso_802.5_token_ring"></span><span id="ISO_802.5_TOKEN_RING"></span>

**ISO 802,5-TokenRing** (9)


</dt> <dd></dd> <dt>

<span id="ISO_802.6_MAN"></span><span id="iso_802.6_man"></span>

**ISO 802,6 Mann** (10)


</dt> <dd></dd> <dt>

<span id="StarLAN"></span><span id="starlan"></span><span id="STARLAN"></span>

**StarLAN** (11)


</dt> <dd></dd> <dt>

<span id="Proteon_10Mbit"></span><span id="proteon_10mbit"></span><span id="PROTEON_10MBIT"></span>

**Schützfür 10Mbit** (12)


</dt> <dd></dd> <dt>

<span id="Proteon_80Mbit"></span><span id="proteon_80mbit"></span><span id="PROTEON_80MBIT"></span>

**Schützlos** (13)


</dt> <dd></dd> <dt>

<span id="HyperChannel"></span><span id="hyperchannel"></span><span id="HYPERCHANNEL"></span>

**Hyperchannel** (14)


</dt> <dd></dd> <dt>

<span id="FDDI"></span><span id="fddi"></span>

**F-di** (15)


</dt> <dd></dd> <dt>

<span id="LAP-B"></span><span id="lap-b"></span>

**Lap-B** (16)


</dt> <dd></dd> <dt>

<span id="SDLC"></span><span id="sdlc"></span>

**SDLC** (17)


</dt> <dd></dd> <dt>

<span id="DS1"></span><span id="ds1"></span>

**Ds1** (18)


</dt> <dd></dd> <dt>

<span id="E1"></span><span id="e1"></span>

**E1** (19)


</dt> <dd></dd> <dt>

<span id="Basic_ISDN"></span><span id="basic_isdn"></span><span id="BASIC_ISDN"></span>

**Basis-ISDN** (20)


</dt> <dd></dd> <dt>

<span id="Primary_ISDN"></span><span id="primary_isdn"></span><span id="PRIMARY_ISDN"></span>

**Primärer ISDN** (21)


</dt> <dd></dd> <dt>

<span id="Proprietary_Point-to-Point_Serial"></span><span id="proprietary_point-to-point_serial"></span><span id="PROPRIETARY_POINT-TO-POINT_SERIAL"></span>

**Proprietäre Punkt-zu-Punkt-seriell** (22)


</dt> <dd></dd> <dt>

<span id="PPP"></span><span id="ppp"></span>

**PPP** (23)


</dt> <dd></dd> <dt>

<span id="Software_Loopback"></span><span id="software_loopback"></span><span id="SOFTWARE_LOOPBACK"></span>

**Software Loopback** (24)


</dt> <dd></dd> <dt>

<span id="EON"></span><span id="eon"></span>

**EON** (25)


</dt> <dd></dd> <dt>

<span id="Ethernet_3Mbit"></span><span id="ethernet_3mbit"></span><span id="ETHERNET_3MBIT"></span>

**Ethernet 3Mbit** (26)


</dt> <dd></dd> <dt>

<span id="NSIP"></span><span id="nsip"></span>

**NSIP** (27)


</dt> <dd></dd> <dt>

<span id="SLIP"></span><span id="slip"></span>

**Slip** (28)


</dt> <dd></dd> <dt>

<span id="Ultra"></span><span id="ultra"></span><span id="ULTRA"></span>

**Ultra** (29)


</dt> <dd></dd> <dt>

<span id="DS3"></span><span id="ds3"></span>

**DS3** (30)


</dt> <dd></dd> <dt>

<span id="SIP"></span><span id="sip"></span>

**SIP** (31)


</dt> <dd></dd> <dt>

<span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>

**Frame Relay** (32)


</dt> <dd></dd> <dt>

<span id="RS-232"></span><span id="rs-232"></span>

**RS-232** (33)


</dt> <dd></dd> <dt>

<span id="Parallel"></span><span id="parallel"></span><span id="PARALLEL"></span>

**Parallel** (34)


</dt> <dd></dd> <dt>

<span id="ARCNet"></span><span id="arcnet"></span><span id="ARCNET"></span>

**ARCNET** (35)


</dt> <dd></dd> <dt>

<span id="ARCNet_Plus"></span><span id="arcnet_plus"></span><span id="ARCNET_PLUS"></span>

**ARCNET Plus** (36)


</dt> <dd></dd> <dt>

<span id="ATM"></span><span id="atm"></span>

**ATM** (37)


</dt> <dd></dd> <dt>

<span id="MIO_X.25"></span><span id="mio_x.25"></span>

**Mio. 25** (38)


</dt> <dd></dd> <dt>

<span id="SONET"></span><span id="sonet"></span>

**SONET** (39)


</dt> <dd></dd> <dt>

<span id="X.25_PLE"></span><span id="x.25_ple"></span>

**X. 25 PLE** (40)


</dt> <dd></dd> <dt>

<span id="ISO_802.211c"></span><span id="iso_802.211c"></span><span id="ISO_802.211C"></span>

**ISO 802.211 c** (41)


</dt> <dd></dd> <dt>

<span id="LocalTalk"></span><span id="localtalk"></span><span id="LOCALTALK"></span>

**LocalTalk** (42)


</dt> <dd></dd> <dt>

<span id="SMDS_DXI"></span><span id="smds_dxi"></span>

**SMDS DXI** (43)


</dt> <dd></dd> <dt>

<span id="Frame_Relay_Service"></span><span id="frame_relay_service"></span><span id="FRAME_RELAY_SERVICE"></span>

**Frame Relay-Dienst** (44)


</dt> <dd></dd> <dt>

<span id="V.35"></span><span id="v.35"></span>

**V. 35** (45)


</dt> <dd></dd> <dt>

<span id="HSSI"></span><span id="hssi"></span>

**HSSI** (46)


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

**HIPPI** (47)


</dt> <dd></dd> <dt>

<span id="Modem"></span><span id="modem"></span><span id="MODEM"></span>

**Modem** (48)


</dt> <dd></dd> <dt>

<span id="AAL5"></span><span id="aal5"></span>

**AAL5** (49)


</dt> <dd></dd> <dt>

<span id="SONET_Path"></span><span id="sonet_path"></span><span id="SONET_PATH"></span>

**Sonetpfad** (50)


</dt> <dd></dd> <dt>

<span id="SONET_VT"></span><span id="sonet_vt"></span>

**SONET VT** (51)


</dt> <dd></dd> <dt>

<span id="SMDS_ICIP"></span><span id="smds_icip"></span>

**SMDS ICIP** (52)


</dt> <dd></dd> <dt>

<span id="Proprietary_Virtual_Internal"></span><span id="proprietary_virtual_internal"></span><span id="PROPRIETARY_VIRTUAL_INTERNAL"></span>

**Proprietäre virtuell/intern** (53)


</dt> <dd></dd> <dt>

<span id="Proprietary_Multiplexor"></span><span id="proprietary_multiplexor"></span><span id="PROPRIETARY_MULTIPLEXOR"></span>

**Proprietäres Multiplexor** (54)


</dt> <dd></dd> <dt>

<span id="IEEE_802.12"></span><span id="ieee_802.12"></span>

**IEEE 802,12** (55)


</dt> <dd></dd> <dt>

<span id="Fibre_Channel"></span><span id="fibre_channel"></span><span id="FIBRE_CHANNEL"></span>

**Fibre Channel** (56)


</dt> <dd></dd> <dt>

<span id="HIPPI_Interface"></span><span id="hippi_interface"></span><span id="HIPPI_INTERFACE"></span>

**HIPPI-Schnittstelle** (57)


</dt> <dd></dd> <dt>

<span id="Frame_Relay_Interconnect"></span><span id="frame_relay_interconnect"></span><span id="FRAME_RELAY_INTERCONNECT"></span>

**Frame Relay-Interconnect** (58)


</dt> <dd></dd> <dt>

<span id="ATM_Emulated_LAN_for_802.3"></span><span id="atm_emulated_lan_for_802.3"></span><span id="ATM_EMULATED_LAN_FOR_802.3"></span>

Mit **ATM emulierten LAN für 802,3** (59)


</dt> <dd></dd> <dt>

<span id="ATM_Emulated_LAN_for_802.5"></span><span id="atm_emulated_lan_for_802.5"></span><span id="ATM_EMULATED_LAN_FOR_802.5"></span>

Mit **ATM emulierten LAN für 802,5** (60)


</dt> <dd></dd> <dt>

<span id="ATM_Emulated_Circuit"></span><span id="atm_emulated_circuit"></span><span id="ATM_EMULATED_CIRCUIT"></span>

Verbindung mit " **ATM-emuliert** " (61)


</dt> <dd></dd> <dt>

<span id="Fast_Ethernet__100BaseT_"></span><span id="fast_ethernet__100baset_"></span><span id="FAST_ETHERNET__100BASET_"></span>

**Schnelles Ethernet (100BaseT)** (62)


</dt> <dd></dd> <dt>

<span id="ISDN"></span><span id="isdn"></span>

**ISDN** (63)


</dt> <dd></dd> <dt>

<span id="V.11"></span><span id="v.11"></span>

**V. 11** (64)


</dt> <dd></dd> <dt>

<span id="V.36"></span><span id="v.36"></span>

**V. 36** (65)


</dt> <dd></dd> <dt>

<span id="G703_at_64K"></span><span id="g703_at_64k"></span><span id="G703_AT_64K"></span>

**G703 bei 64K** (66)


</dt> <dd></dd> <dt>

<span id="G703_at_2Mb"></span><span id="g703_at_2mb"></span><span id="G703_AT_2MB"></span>

**G703 bei 2 MB** (67)


</dt> <dd></dd> <dt>

<span id="QLLC"></span><span id="qllc"></span>

**QLLC** (68)


</dt> <dd></dd> <dt>

<span id="Fast_Ethernet_100BaseFX"></span><span id="fast_ethernet_100basefx"></span><span id="FAST_ETHERNET_100BASEFX"></span>

**Schnelles Ethernet 100BaseFX** (69)


</dt> <dd></dd> <dt>

<span id="Channel"></span><span id="channel"></span><span id="CHANNEL"></span>

**Channel** (70)


</dt> <dd></dd> <dt>

<span id="IEEE_802.11"></span><span id="ieee_802.11"></span>

**IEEE 802,11** (71)


</dt> <dd></dd> <dt>

<span id="IBM_260_370_OEMI_Channel"></span><span id="ibm_260_370_oemi_channel"></span><span id="IBM_260_370_OEMI_CHANNEL"></span>

**IBM 260/370-Kanal (oemi** ) (72)


</dt> <dd></dd> <dt>

<span id="ESCON"></span><span id="escon"></span>

**ESCON** (73)


</dt> <dd></dd> <dt>

<span id="Data_Link_Switching"></span><span id="data_link_switching"></span><span id="DATA_LINK_SWITCHING"></span>

**Daten Link Wechsel** (74)


</dt> <dd></dd> <dt>

<span id="ISDN_S_T_Interface"></span><span id="isdn_s_t_interface"></span><span id="ISDN_S_T_INTERFACE"></span>

**ISDN S/T-Schnittstelle** (75)


</dt> <dd></dd> <dt>

<span id="ISDN_U_Interface"></span><span id="isdn_u_interface"></span><span id="ISDN_U_INTERFACE"></span>

**ISDN-U-Schnittstelle** (76)


</dt> <dd></dd> <dt>

<span id="LAP-D"></span><span id="lap-d"></span>

**Lap-D** (77)


</dt> <dd></dd> <dt>

<span id="IP_Switch"></span><span id="ip_switch"></span><span id="IP_SWITCH"></span>

**IP-Switch** (78)


</dt> <dd></dd> <dt>

<span id="Remote_Source_Route_Bridging"></span><span id="remote_source_route_bridging"></span><span id="REMOTE_SOURCE_ROUTE_BRIDGING"></span>

**Remote-Quell Routen Überbrückung** (79)


</dt> <dd></dd> <dt>

<span id="ATM_Logical"></span><span id="atm_logical"></span><span id="ATM_LOGICAL"></span>

**ATM logisch** (80)


</dt> <dd></dd> <dt>

<span id="DS0"></span><span id="ds0"></span>

**DS0** (81)


</dt> <dd></dd> <dt>

<span id="DS0_Bundle"></span><span id="ds0_bundle"></span><span id="DS0_BUNDLE"></span>

**DS0 Bundle** (82)


</dt> <dd></dd> <dt>

<span id="BSC"></span><span id="bsc"></span>

**BSC** (83)


</dt> <dd></dd> <dt>

<span id="Async"></span><span id="async"></span><span id="ASYNC"></span>

**Async** (84)


</dt> <dd></dd> <dt>

<span id="Combat_Net_Radio"></span><span id="combat_net_radio"></span><span id="COMBAT_NET_RADIO"></span>

**Netzwerk Radio** (85)


</dt> <dd></dd> <dt>

<span id="ISO_802.5r_DTR"></span><span id="iso_802.5r_dtr"></span><span id="ISO_802.5R_DTR"></span>

**ISO 802.5 definiert r DTR** (86)


</dt> <dd></dd> <dt>

<span id="Ext_Pos_Loc_Report_System"></span><span id="ext_pos_loc_report_system"></span><span id="EXT_POS_LOC_REPORT_SYSTEM"></span>

**Ext POS Loc-Berichts System** (87)


</dt> <dd></dd> <dt>

<span id="AppleTalk_Remote_Access_Protocol"></span><span id="appletalk_remote_access_protocol"></span><span id="APPLETALK_REMOTE_ACCESS_PROTOCOL"></span>

**AppleTalk-Remote Zugriffsprotokoll** (88)


</dt> <dd></dd> <dt>

<span id="Proprietary_Connectionless"></span><span id="proprietary_connectionless"></span><span id="PROPRIETARY_CONNECTIONLESS"></span>

**Proprietäre Connectionless** (89)


</dt> <dd></dd> <dt>

<span id="ITU_X.29_Host_PAD"></span><span id="itu_x.29_host_pad"></span><span id="ITU_X.29_HOST_PAD"></span>

**ITU X. 29-hostpad** (90)


</dt> <dd></dd> <dt>

<span id="ITU_X.3_Terminal_PAD"></span><span id="itu_x.3_terminal_pad"></span><span id="ITU_X.3_TERMINAL_PAD"></span>

**ITU X. 3-Terminal Pad** (91)


</dt> <dd></dd> <dt>

<span id="Frame_Relay_MPI"></span><span id="frame_relay_mpi"></span><span id="FRAME_RELAY_MPI"></span>

**Frame Relay MPI** (92)


</dt> <dd></dd> <dt>

<span id="ITU_X.213"></span><span id="itu_x.213"></span>

**ITU X. 213** (93)


</dt> <dd></dd> <dt>

<span id="ADSL"></span><span id="adsl"></span>

**ADSL** (94)


</dt> <dd></dd> <dt>

<span id="RADSL"></span><span id="radsl"></span>

**RADSL** (95)


</dt> <dd></dd> <dt>

<span id="SDSL"></span><span id="sdsl"></span>

**SDSL** (96)


</dt> <dd></dd> <dt>

<span id="VDSL"></span><span id="vdsl"></span>

**VDSL** (97)


</dt> <dd></dd> <dt>

<span id="ISO_802.5_CRFP"></span><span id="iso_802.5_crfp"></span>

**ISO 802,5 crfp** (98)


</dt> <dd></dd> <dt>

<span id="Myrinet"></span><span id="myrinet"></span><span id="MYRINET"></span>

**Myrinet** (99)


</dt> <dd></dd> <dt>

<span id="Voice_Receive_and_Transmit"></span><span id="voice_receive_and_transmit"></span><span id="VOICE_RECEIVE_AND_TRANSMIT"></span>

**Sprach Empfang und-Übertragung** (100)


</dt> <dd></dd> <dt>

<span id="Voice_Foreign_Exchange_Office"></span><span id="voice_foreign_exchange_office"></span><span id="VOICE_FOREIGN_EXCHANGE_OFFICE"></span>

**Sprach fremde Exchange-Niederlassung** (101)


</dt> <dd></dd> <dt>

<span id="Voice_Foreign_Exchange_Service"></span><span id="voice_foreign_exchange_service"></span><span id="VOICE_FOREIGN_EXCHANGE_SERVICE"></span>

**Sprachnachrichten Austauschdienst** (102)


</dt> <dd></dd> <dt>

<span id="Voice_Encapsulation"></span><span id="voice_encapsulation"></span><span id="VOICE_ENCAPSULATION"></span>

**Sprach Kapselung** (103)


</dt> <dd></dd> <dt>

<span id="Voice_over_IP"></span><span id="voice_over_ip"></span><span id="VOICE_OVER_IP"></span>

**Voice-over-IP** (104)


</dt> <dd></dd> <dt>

<span id="ATM_DXI"></span><span id="atm_dxi"></span>

**ATM DXI** (105)


</dt> <dd></dd> <dt>

<span id="ATM_FUNI"></span><span id="atm_funi"></span>

**ATM Funi** (106)


</dt> <dd></dd> <dt>

<span id="ATM_IMA"></span><span id="atm_ima"></span>

**ATM IMA** (107)


</dt> <dd></dd> <dt>

<span id="PPP_Multilink_Bundle"></span><span id="ppp_multilink_bundle"></span><span id="PPP_MULTILINK_BUNDLE"></span>

**PPP-multilinkbündel** (108)


</dt> <dd></dd> <dt>

<span id="IP_over_CDLC"></span><span id="ip_over_cdlc"></span><span id="IP_OVER_CDLC"></span>

**IP über CDLC** (109)


</dt> <dd></dd> <dt>

<span id="IP_over_CLAW"></span><span id="ip_over_claw"></span><span id="IP_OVER_CLAW"></span>

**IP-over-Claw** (110)


</dt> <dd></dd> <dt>

<span id="Stack_to_Stack"></span><span id="stack_to_stack"></span><span id="STACK_TO_STACK"></span>

**Stapel zu Stapel** (111)


</dt> <dd></dd> <dt>

<span id="Virtual_IP_Address"></span><span id="virtual_ip_address"></span><span id="VIRTUAL_IP_ADDRESS"></span>

**Virtuelle IP-Adresse** (112)


</dt> <dd></dd> <dt>

<span id="MPC"></span><span id="mpc"></span>

**MPC** (113)


</dt> <dd></dd> <dt>

<span id="IP_over_ATM"></span><span id="ip_over_atm"></span><span id="IP_OVER_ATM"></span>

**IP über ATM** (114)


</dt> <dd></dd> <dt>

<span id="ISO_802.5j_Fibre_Token_Ring"></span><span id="iso_802.5j_fibre_token_ring"></span><span id="ISO_802.5J_FIBRE_TOKEN_RING"></span>

**ISO 802.5 definiert j Fibre Token Ring** (115)


</dt> <dd></dd> <dt>

<span id="TDLC"></span><span id="tdlc"></span>

**Tdlc** (116)


</dt> <dd></dd> <dt>

<span id="Gigabit_Ethernet"></span><span id="gigabit_ethernet"></span><span id="GIGABIT_ETHERNET"></span>

**Gigabit-Ethernet** (117)


</dt> <dd></dd> <dt>

<span id="HDLC"></span><span id="hdlc"></span>

**HDLC** (118)


</dt> <dd></dd> <dt>

<span id="LAP-F"></span><span id="lap-f"></span>

**Lap-F** (119)


</dt> <dd></dd> <dt>

<span id="V.37"></span><span id="v.37"></span>

**V. 37** (120)


</dt> <dd></dd> <dt>

<span id="X.25_MLP"></span><span id="x.25_mlp"></span>

**X. 25 MLP** (121)


</dt> <dd></dd> <dt>

<span id="X.25_Hunt_Group"></span><span id="x.25_hunt_group"></span><span id="X.25_HUNT_GROUP"></span>

**X. 25-Jagdgruppe** (122)


</dt> <dd></dd> <dt>

<span id="Transp_HDLC"></span><span id="transp_hdlc"></span><span id="TRANSP_HDLC"></span>

**Transp HDLC** (123)


</dt> <dd></dd> <dt>

<span id="Interleave_Channel"></span><span id="interleave_channel"></span><span id="INTERLEAVE_CHANNEL"></span>

**Interleave-Kanal** (124)


</dt> <dd></dd> <dt>

<span id="FAST_Channel"></span><span id="fast_channel"></span><span id="FAST_CHANNEL"></span>

**Schneller Kanal** (125)


</dt> <dd></dd> <dt>

<span id="IP__for_APPN_HPR_in_IP_Networks_"></span><span id="ip__for_appn_hpr_in_ip_networks_"></span><span id="IP__FOR_APPN_HPR_IN_IP_NETWORKS_"></span>

**IP (für APPN HPR in IP-Netzwerken)** (126)


</dt> <dd></dd> <dt>

<span id="CATV_MAC_Layer"></span><span id="catv_mac_layer"></span><span id="CATV_MAC_LAYER"></span>

Hyper- **v-Mac-Ebene** (127)


</dt> <dd></dd> <dt>

<span id="CATV_Downstream"></span><span id="catv_downstream"></span><span id="CATV_DOWNSTREAM"></span>

**Streamv Downstream** (128)


</dt> <dd></dd> <dt>

<span id="CATV_Upstream"></span><span id="catv_upstream"></span><span id="CATV_UPSTREAM"></span>

**Streamv Upstream** (129)


</dt> <dd></dd> <dt>

<span id="Avalon_12MPP_Switch"></span><span id="avalon_12mpp_switch"></span><span id="AVALON_12MPP_SWITCH"></span>

**Schalter "Avalon 12mpp** " (130)


</dt> <dd></dd> <dt>

<span id="Tunnel"></span><span id="tunnel"></span><span id="TUNNEL"></span>

**Tunnel** (131)


</dt> <dd></dd> <dt>

<span id="Coffee"></span><span id="coffee"></span><span id="COFFEE"></span>

**Kaffee** (132)


</dt> <dd></dd> <dt>

<span id="Circuit_Emulation_Service"></span><span id="circuit_emulation_service"></span><span id="CIRCUIT_EMULATION_SERVICE"></span>

**Circuit Emulation-Dienst** (133)


</dt> <dd></dd> <dt>

<span id="ATM_SubInterface"></span><span id="atm_subinterface"></span><span id="ATM_SUBINTERFACE"></span>

**ATM-Unterschnittstelle** (134)


</dt> <dd></dd> <dt>

<span id="Layer_2_VLAN_using_802.1Q"></span><span id="layer_2_vlan_using_802.1q"></span><span id="LAYER_2_VLAN_USING_802.1Q"></span>

**Layer 2-VLAN mit 802.1 q** (135)


</dt> <dd></dd> <dt>

<span id="Layer_3_VLAN_using_IP"></span><span id="layer_3_vlan_using_ip"></span><span id="LAYER_3_VLAN_USING_IP"></span>

**Layer 3-VLAN mit IP** (136)


</dt> <dd></dd> <dt>

<span id="Layer_3_VLAN_using_IPX"></span><span id="layer_3_vlan_using_ipx"></span><span id="LAYER_3_VLAN_USING_IPX"></span>

**Layer 3-VLAN mit IPX** (137)


</dt> <dd></dd> <dt>

<span id="Digital_Power_Line"></span><span id="digital_power_line"></span><span id="DIGITAL_POWER_LINE"></span>

**Digitale Stromversorgung** (138)


</dt> <dd></dd> <dt>

<span id="Multimedia_Mail_over_IP"></span><span id="multimedia_mail_over_ip"></span><span id="MULTIMEDIA_MAIL_OVER_IP"></span>

**Multimedia-e-Mail über IP** (139)


</dt> <dd></dd> <dt>

<span id="DTM"></span><span id="dtm"></span>

**DTM** (140)


</dt> <dd></dd> <dt>

<span id="DCN"></span><span id="dcn"></span>

**DCN** (141)


</dt> <dd></dd> <dt>

<span id="IP_Forwarding"></span><span id="ip_forwarding"></span><span id="IP_FORWARDING"></span>

**IP-Weiterleitung** (142)


</dt> <dd></dd> <dt>

<span id="MSDSL"></span><span id="msdsl"></span>

**Msdsl** (143)


</dt> <dd></dd> <dt>

<span id="IEEE_1394"></span><span id="ieee_1394"></span>

**IEEE 1394** (144)


</dt> <dd></dd> <dt>

<span id="IF-GSN_HIPPI-6400"></span><span id="if-gsn_hippi-6400"></span>

**If-GSN/HIPPI-6400** (145)


</dt> <dd></dd> <dt>

<span id="DVB-RCC_MAC_Layer"></span><span id="dvb-rcc_mac_layer"></span><span id="DVB-RCC_MAC_LAYER"></span>

**DVB-RCC Mac-Ebene** (146)


</dt> <dd></dd> <dt>

<span id="DVB-RCC_Downstream"></span><span id="dvb-rcc_downstream"></span><span id="DVB-RCC_DOWNSTREAM"></span>

**DVB-RCC Downstream** (147)


</dt> <dd></dd> <dt>

<span id="DVB-RCC_Upstream"></span><span id="dvb-rcc_upstream"></span><span id="DVB-RCC_UPSTREAM"></span>

**DVB-RCC Upstream** (148)


</dt> <dd></dd> <dt>

<span id="ATM_Virtual"></span><span id="atm_virtual"></span><span id="ATM_VIRTUAL"></span>

**ATM virtuell** (149)


</dt> <dd></dd> <dt>

<span id="MPLS_Tunnel"></span><span id="mpls_tunnel"></span><span id="MPLS_TUNNEL"></span>

**MPLS-Tunnel** (150)


</dt> <dd></dd> <dt>

<span id="SRP"></span><span id="srp"></span>

**SRP** (151)


</dt> <dd></dd> <dt>

<span id="Voice_over_ATM"></span><span id="voice_over_atm"></span><span id="VOICE_OVER_ATM"></span>

**Voice over ATM** (152)


</dt> <dd></dd> <dt>

<span id="Voice_over_Frame_Relay"></span><span id="voice_over_frame_relay"></span><span id="VOICE_OVER_FRAME_RELAY"></span>

**Voice over Frame Relay** (153)


</dt> <dd></dd> <dt>

<span id="ISDL"></span><span id="isdl"></span>

**Isdl** (154)


</dt> <dd></dd> <dt>

<span id="Composite_Link"></span><span id="composite_link"></span><span id="COMPOSITE_LINK"></span>

**Zusammengesetzter Link** (155)


</dt> <dd></dd> <dt>

<span id="SS7_Signaling_Link"></span><span id="ss7_signaling_link"></span><span id="SS7_SIGNALING_LINK"></span>

**SS7 Signalisierungs Link** (156)


</dt> <dd></dd> <dt>

<span id="Proprietary_P2P_Wireless"></span><span id="proprietary_p2p_wireless"></span><span id="PROPRIETARY_P2P_WIRELESS"></span>

**Proprietäre P2P Wireless** (157)


</dt> <dd></dd> <dt>

<span id="Frame_Forward"></span><span id="frame_forward"></span><span id="FRAME_FORWARD"></span>

**Frame vorwärts** (158)


</dt> <dd></dd> <dt>

<span id="RFC1483_Multiprotocol_over_ATM"></span><span id="rfc1483_multiprotocol_over_atm"></span><span id="RFC1483_MULTIPROTOCOL_OVER_ATM"></span>

**RFC1483 MultiProtocol über ATM** (159)


</dt> <dd></dd> <dt>

<span id="USB"></span><span id="usb"></span>

**USB** (160)


</dt> <dd></dd> <dt>

<span id="IEEE_802.3ad_Link_Aggregate"></span><span id="ieee_802.3ad_link_aggregate"></span><span id="IEEE_802.3AD_LINK_AGGREGATE"></span>

**IEEE 802.3 Ad-Link Aggregat** (161)


</dt> <dd></dd> <dt>

<span id="BGP_Policy_Accounting"></span><span id="bgp_policy_accounting"></span><span id="BGP_POLICY_ACCOUNTING"></span>

**BGP-Richtlinien Abrechnung** (162)


</dt> <dd></dd> <dt>

<span id="FRF_.16_Multilink_FR"></span><span id="frf_.16_multilink_fr"></span><span id="FRF_.16_MULTILINK_FR"></span>

**FRF .16 Multilink fr** (163)


</dt> <dd></dd> <dt>

<span id="H.323_Gatekeeper"></span><span id="h.323_gatekeeper"></span><span id="H.323_GATEKEEPER"></span>

**H. 323 Gatekeeper** (164)


</dt> <dd></dd> <dt>

<span id="H.323_Proxy"></span><span id="h.323_proxy"></span><span id="H.323_PROXY"></span>

**H. 323-Proxy** (165)


</dt> <dd></dd> <dt>

<span id="MPLS"></span><span id="mpls"></span>

**MPLS** (166)


</dt> <dd></dd> <dt>

<span id="Multi-Frequency_Signaling_Link"></span><span id="multi-frequency_signaling_link"></span><span id="MULTI-FREQUENCY_SIGNALING_LINK"></span>

**Mehrfach Frequenz-Signal Verknüpfung** (167)


</dt> <dd></dd> <dt>

<span id="HDSL-2"></span><span id="hdsl-2"></span>

**HDSL-2** (168)


</dt> <dd></dd> <dt>

<span id="S-HDSL"></span><span id="s-hdsl"></span>

**S-HDSL** (169)


</dt> <dd></dd> <dt>

<span id="DS1_Facility_Data_Link"></span><span id="ds1_facility_data_link"></span><span id="DS1_FACILITY_DATA_LINK"></span>

**Ds1-Anlagedaten Link** (170)


</dt> <dd></dd> <dt>

<span id="Packet_over_SONET_SDH"></span><span id="packet_over_sonet_sdh"></span><span id="PACKET_OVER_SONET_SDH"></span>

**Paket über SONET/SDH** (171)


</dt> <dd></dd> <dt>

<span id="DVB-ASI_Input"></span><span id="dvb-asi_input"></span><span id="DVB-ASI_INPUT"></span>

**DVB-ASI-Eingabe** (172)


</dt> <dd></dd> <dt>

<span id="DVB-ASI_Output"></span><span id="dvb-asi_output"></span><span id="DVB-ASI_OUTPUT"></span>

**DVB-ASI-Ausgabe** (173)


</dt> <dd></dd> <dt>

<span id="Power_Line"></span><span id="power_line"></span><span id="POWER_LINE"></span>

**Stromversorgung** (174)


</dt> <dd></dd> <dt>

<span id="Non_Facility_Associated_Signaling"></span><span id="non_facility_associated_signaling"></span><span id="NON_FACILITY_ASSOCIATED_SIGNALING"></span>

**Nicht der Anlage zugeordnete Signalisierung** (175)


</dt> <dd></dd> <dt>

<span id="TR008"></span><span id="tr008"></span>

**TR008** (176)


</dt> <dd></dd> <dt>

<span id="GR303_RDT"></span><span id="gr303_rdt"></span>

**GR303 RDT** (177)


</dt> <dd></dd> <dt>

<span id="GR303_IDT"></span><span id="gr303_idt"></span>

**GR303 IDT** (178)


</dt> <dd></dd> <dt>

<span id="ISUP"></span><span id="isup"></span>

**IsUp** (179)


</dt> <dd></dd> <dt>

<span id="Proprietary_Wireless_MAC_Layer"></span><span id="proprietary_wireless_mac_layer"></span><span id="PROPRIETARY_WIRELESS_MAC_LAYER"></span>

**Proprietäre drahtlose Mac-Ebene** (180)


</dt> <dd></dd> <dt>

<span id="Proprietary_Wireless_Downstream"></span><span id="proprietary_wireless_downstream"></span><span id="PROPRIETARY_WIRELESS_DOWNSTREAM"></span>

**Proprietäre drahtlos, Downstream** (181)


</dt> <dd></dd> <dt>

<span id="Proprietary_Wireless_Upstream"></span><span id="proprietary_wireless_upstream"></span><span id="PROPRIETARY_WIRELESS_UPSTREAM"></span>

**Proprietäre drahtlos Upstream** (182)


</dt> <dd></dd> <dt>

<span id="HIPERLAN_Type_2"></span><span id="hiperlan_type_2"></span><span id="HIPERLAN_TYPE_2"></span>

**HIPERLAN-Typ 2** (183)


</dt> <dd></dd> <dt>

<span id="Proprietary_Broadband_Wireless_Access_Point_to_Mulipoint"></span><span id="proprietary_broadband_wireless_access_point_to_mulipoint"></span><span id="PROPRIETARY_BROADBAND_WIRELESS_ACCESS_POINT_TO_MULIPOINT"></span>

Geschützter **Breitband-drahtlos Zugriffspunkt auf mulipoint** (184)


</dt> <dd></dd> <dt>

<span id="SONET_Overhead_Channel"></span><span id="sonet_overhead_channel"></span><span id="SONET_OVERHEAD_CHANNEL"></span>

**SONET-Overhead-Kanal** (185)


</dt> <dd></dd> <dt>

<span id="Digital_Wrapper_Overhead_Channel"></span><span id="digital_wrapper_overhead_channel"></span><span id="DIGITAL_WRAPPER_OVERHEAD_CHANNEL"></span>

Verwaltungs Kanal für den **digitalen Wrapper** (186)


</dt> <dd></dd> <dt>

<span id="ATM_Adaptation_Layer_2"></span><span id="atm_adaptation_layer_2"></span><span id="ATM_ADAPTATION_LAYER_2"></span>

**ATM-Anpassungs Schicht 2** (187)


</dt> <dd></dd> <dt>

<span id="Radio_MAC"></span><span id="radio_mac"></span><span id="RADIO_MAC"></span>

**Radio Mac** (188)


</dt> <dd></dd> <dt>

<span id="ATM_Radio"></span><span id="atm_radio"></span><span id="ATM_RADIO"></span>

**ATM Radio** (189)


</dt> <dd></dd> <dt>

<span id="Inter_Machine_Trunk"></span><span id="inter_machine_trunk"></span><span id="INTER_MACHINE_TRUNK"></span>

**Trunk zwischen Computer** (190)


</dt> <dd></dd> <dt>

<span id="MVL_DSL"></span><span id="mvl_dsl"></span>

**Mvl-DSL** (191)


</dt> <dd></dd> <dt>

<span id="Long_Read_DSL"></span><span id="long_read_dsl"></span><span id="LONG_READ_DSL"></span>

**Lange Lese-DSL** (192)


</dt> <dd></dd> <dt>

<span id="Frame_Relay_DLCI_Endpoint"></span><span id="frame_relay_dlci_endpoint"></span><span id="FRAME_RELAY_DLCI_ENDPOINT"></span>

**Rahmen Relay-DLCI-Endpunkt** (193)


</dt> <dd></dd> <dt>

<span id="ATM_VCI_Endpoint"></span><span id="atm_vci_endpoint"></span><span id="ATM_VCI_ENDPOINT"></span>

**ATM-VCI-Endpunkt** (194)


</dt> <dd></dd> <dt>

<span id="Optical_Channel"></span><span id="optical_channel"></span><span id="OPTICAL_CHANNEL"></span>

**Optischer Kanal** (195)


</dt> <dd></dd> <dt>

<span id="Optical_Transport"></span><span id="optical_transport"></span><span id="OPTICAL_TRANSPORT"></span>

**Optischer Transport** (196)


</dt> <dd></dd> <dt>

<span id="Proprietary_ATM"></span><span id="proprietary_atm"></span><span id="PROPRIETARY_ATM"></span>

**Proprietäre ATM** (197)


</dt> <dd></dd> <dt>

<span id="Voice_over_Cable"></span><span id="voice_over_cable"></span><span id="VOICE_OVER_CABLE"></span>

**Voice-over-Kabel** (198)


</dt> <dd></dd> <dt>

<span id="Infiniband"></span><span id="infiniband"></span><span id="INFINIBAND"></span>

**InfiniBand** (199)


</dt> <dd></dd> <dt>

<span id="TE_Link"></span><span id="te_link"></span><span id="TE_LINK"></span>

**Te-Verknüpfung** (200)


</dt> <dd></dd> <dt>

<span id="Q.2931"></span><span id="q.2931"></span>

**Q. 2931** (201)


</dt> <dd></dd> <dt>

<span id="Virtual_Trunk_Group"></span><span id="virtual_trunk_group"></span><span id="VIRTUAL_TRUNK_GROUP"></span>

**Virtuelle Trunk Gruppe** (202)


</dt> <dd></dd> <dt>

<span id="SIP_Trunk_Group"></span><span id="sip_trunk_group"></span><span id="SIP_TRUNK_GROUP"></span>

**SIP-Trunk Gruppe** (203)


</dt> <dd></dd> <dt>

<span id="SIP_Signaling"></span><span id="sip_signaling"></span><span id="SIP_SIGNALING"></span>

**SIP-Signalisierung** (204)


</dt> <dd></dd> <dt>

<span id="CATV_Upstream_Channel"></span><span id="catv_upstream_channel"></span><span id="CATV_UPSTREAM_CHANNEL"></span>

**Streamv-upstreamchannel** (205)


</dt> <dd></dd> <dt>

<span id="Econet"></span><span id="econet"></span><span id="ECONET"></span>

**Econet** (206)


</dt> <dd></dd> <dt>

<span id="FSAN_155Mb_PON"></span><span id="fsan_155mb_pon"></span><span id="FSAN_155MB_PON"></span>

**F** -5-MB-Pon (207)


</dt> <dd></dd> <dt>

<span id="FSAN_622Mb_PON"></span><span id="fsan_622mb_pon"></span><span id="FSAN_622MB_PON"></span>

**F 622mb Pon** (208)


</dt> <dd></dd> <dt>

<span id="Transparent_Bridge"></span><span id="transparent_bridge"></span><span id="TRANSPARENT_BRIDGE"></span>

**Transparente Brücke** (209)


</dt> <dd></dd> <dt>

<span id="Line_Group"></span><span id="line_group"></span><span id="LINE_GROUP"></span>

**Zeilen Gruppe** (210)


</dt> <dd></dd> <dt>

<span id="Voice_E_M_Feature_Group"></span><span id="voice_e_m_feature_group"></span><span id="VOICE_E_M_FEATURE_GROUP"></span>

**Sprach-E&M-Funktionsgruppe** (211)


</dt> <dd></dd> <dt>

<span id="Voice_FGD_EANA"></span><span id="voice_fgd_eana"></span><span id="VOICE_FGD_EANA"></span>

**Sprach-f-Eana** (212)


</dt> <dd></dd> <dt>

<span id="Voice_DID"></span><span id="voice_did"></span><span id="VOICE_DID"></span>

**Stimme** an (213)


</dt> <dd></dd> <dt>

<span id="MPEG_Transport"></span><span id="mpeg_transport"></span><span id="MPEG_TRANSPORT"></span>

**MPEG-Transport** (214)


</dt> <dd></dd> <dt>

<span id="6To4"></span><span id="6to4"></span><span id="6TO4"></span>

**6zu 4** (215)


</dt> <dd></dd> <dt>

<span id="GTP"></span><span id="gtp"></span>

**GTP** (216)


</dt> <dd></dd> <dt>

<span id="Paradyne_EtherLoop_1"></span><span id="paradyne_etherloop_1"></span><span id="PARADYNE_ETHERLOOP_1"></span>

**Paradyne etherloop 1** (217)


</dt> <dd></dd> <dt>

<span id="Paradyne_EtherLoop_2"></span><span id="paradyne_etherloop_2"></span><span id="PARADYNE_ETHERLOOP_2"></span>

**Paradyne etherloop 2** (218)


</dt> <dd></dd> <dt>

<span id="Optical_Channel_Group"></span><span id="optical_channel_group"></span><span id="OPTICAL_CHANNEL_GROUP"></span>

**Optische Kanal Gruppe** (219)


</dt> <dd></dd> <dt>

<span id="HomePNA"></span><span id="homepna"></span><span id="HOMEPNA"></span>

**HomePNA** (220)


</dt> <dd></dd> <dt>

<span id="GFP"></span><span id="gfp"></span>

**GFP** (221)


</dt> <dd></dd> <dt>

<span id="ciscoISLvlan"></span><span id="ciscoislvlan"></span><span id="CISCOISLVLAN"></span>

**ciscoislvlan** (222)


</dt> <dd></dd> <dt>

<span id="actelisMetaLOOP"></span><span id="actelismetaloop"></span><span id="ACTELISMETALOOP"></span>

**actelismetaloop** (223)


</dt> <dd></dd> <dt>

<span id="Fcip"></span><span id="fcip"></span><span id="FCIP"></span>

**F** (224)


</dt> <dd></dd> <dt>

<span id="IANA_Reserved"></span><span id="iana_reserved"></span><span id="IANA_RESERVED"></span>

**IANA reserviert** (225.. 4095)


</dt> <dd></dd> <dt>

<span id="IPv4"></span><span id="ipv4"></span><span id="IPV4"></span>

**IPv4** (4096)


</dt> <dd></dd> <dt>

<span id="IPv6"></span><span id="ipv6"></span><span id="IPV6"></span>

**IPv6** (4097)


</dt> <dd></dd> <dt>

<span id="IPv4_v6"></span><span id="ipv4_v6"></span><span id="IPV4_V6"></span>

**IPv4/V6** (4098)


</dt> <dd></dd> <dt>

<span id="IPX"></span><span id="ipx"></span>

**IPX** (4099)


</dt> <dd></dd> <dt>

<span id="DECnet"></span><span id="decnet"></span><span id="DECNET"></span>

**DECnet** (4100)


</dt> <dd></dd> <dt>

<span id="SNA"></span><span id="sna"></span>

**SNA** (4101)


</dt> <dd></dd> <dt>

<span id="CONP"></span><span id="conp"></span>

Verbindungs- **Manager (4102** )


</dt> <dd></dd> <dt>

<span id="CLNP"></span><span id="clnp"></span>

**CLNP** (4103)


</dt> <dd></dd> <dt>

<span id="VINES"></span><span id="vines"></span>

**Rebstöcke** (4104)


</dt> <dd></dd> <dt>

<span id="XNS"></span><span id="xns"></span>

**XNS** (4105)


</dt> <dd></dd> <dt>

<span id="ISDN_B_Channel_Endpoint"></span><span id="isdn_b_channel_endpoint"></span><span id="ISDN_B_CHANNEL_ENDPOINT"></span>

**ISDN-B-Kanal Endpunkt** (4106)


</dt> <dd></dd> <dt>

<span id="ISDN_D_Channel_Endpoint"></span><span id="isdn_d_channel_endpoint"></span><span id="ISDN_D_CHANNEL_ENDPOINT"></span>

**ISDN-D-Kanal Endpunkt** (4107)


</dt> <dd></dd> <dt>

<span id="BGP"></span><span id="bgp"></span>

**BGP** (4108)


</dt> <dd></dd> <dt>

<span id="OSPF"></span><span id="ospf"></span>

**OSPF** (4109)


</dt> <dd></dd> <dt>

<span id="UDP"></span><span id="udp"></span>

**UDP** (4110)


</dt> <dd></dd> <dt>

<span id="TCP"></span><span id="tcp"></span>

**TCP** (4111)


</dt> <dd></dd> <dt>

<span id="802.11a"></span><span id="802.11A"></span>

**802.11 a** (4112)


</dt> <dd></dd> <dt>

<span id="802.11b"></span><span id="802.11B"></span>

**802.11 b** (4113)


</dt> <dd></dd> <dt>

<span id="802.11g"></span><span id="802.11G"></span>

**802.11 g** (4114)


</dt> <dd></dd> <dt>

<span id="802.11h"></span><span id="802.11H"></span>

**802.11 h** (4115)


</dt> <dd></dd> <dt>

<span id="NFS"></span><span id="nfs"></span>

**NFS** (4200)


</dt> <dd></dd> <dt>

<span id="CIFS"></span><span id="cifs"></span>

**CIFS** (4201)


</dt> <dd></dd> <dt>

<span id="DAFS"></span><span id="dafs"></span>

**DAFS** (4202)


</dt> <dd></dd> <dt>

<span id="WebDAV"></span><span id="webdav"></span><span id="WEBDAV"></span>

**WebDAV** (4203)


</dt> <dd></dd> <dt>

<span id="HTTP"></span><span id="http"></span>

**Http** (4204)


</dt> <dd></dd> <dt>

<span id="FTP"></span><span id="ftp"></span>

**FTP** (4205)


</dt> <dd></dd> <dt>

<span id="NDMP"></span><span id="ndmp"></span>

**NDMP** (4300)


</dt> <dd></dd> <dt>

<span id="Telnet"></span><span id="telnet"></span><span id="TELNET"></span>

**Telnet** (4400)


</dt> <dd></dd> <dt>

<span id="SSH"></span><span id="ssh"></span>

**SSH** (4401)


</dt> <dd></dd> <dt>

<span id="SM_CLP"></span><span id="sm_clp"></span>

**SM CLP** (4402)


</dt> <dd></dd> <dt>

<span id="SMTP"></span><span id="smtp"></span>

**SMTP** (4403)


</dt> <dd></dd> <dt>

<span id="LDAP"></span><span id="ldap"></span>

**LDAP** (4404)


</dt> <dd></dd> <dt>

<span id="RDP"></span><span id="rdp"></span>

**RDP** (4405)


</dt> <dd></dd> <dt>

<span id="HTTPS"></span><span id="https"></span>

**Https** (4406)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reserviert** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Anbieter reserviert** (32768..)


</dt> <dd></dd> </dl>

</dd> <dt>

**ProtocolType**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**CIM \_ protocolendpoint**.**Protocoliftype**"), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ protocolendpoint**".**OtherTypeDescription**")
</dt> </dl>

> [!Note]  
> Veraltete Beschreibung: eine Enumeration, die verwendet wird, um verschiedene Instanzen dieser Klasse zu kategorisieren und zu klassifizieren.

 

Diese Eigenschaft ist veraltet. Verwenden Sie stattdessen die **protocoliftype** -Eigenschaft.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Sonstige** (1)


</dt> <dd></dd> <dt>

<span id="IPv4"></span><span id="ipv4"></span><span id="IPV4"></span>

**IPv4** (2)


</dt> <dd></dd> <dt>

<span id="IPv6"></span><span id="ipv6"></span><span id="IPV6"></span>

**IPv6** (3)


</dt> <dd></dd> <dt>

<span id="IPX"></span><span id="ipx"></span>

**IPX** (4)


</dt> <dd></dd> <dt>

<span id="AppleTalk"></span><span id="appletalk"></span><span id="APPLETALK"></span>

**AppleTalk** (5)


</dt> <dd></dd> <dt>

<span id="DECnet"></span><span id="decnet"></span><span id="DECNET"></span>

**DECnet** (6)


</dt> <dd></dd> <dt>

<span id="SNA"></span><span id="sna"></span>

**SNA** (7)


</dt> <dd></dd> <dt>

<span id="CONP"></span><span id="conp"></span>

Verbindung **(8** )


</dt> <dd></dd> <dt>

<span id="CLNP"></span><span id="clnp"></span>

**CLNP** (9)


</dt> <dd></dd> <dt>

<span id="VINES"></span><span id="vines"></span>

**Rebstöcke** (10)


</dt> <dd></dd> <dt>

<span id="XNS"></span><span id="xns"></span>

**XNS** (11)


</dt> <dd></dd> <dt>

<span id="ATM"></span><span id="atm"></span>

**ATM** (12)


</dt> <dd></dd> <dt>

<span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>

**Frame Relay** (13)


</dt> <dd></dd> <dt>

<span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>

**Ethernet** (14)


</dt> <dd></dd> <dt>

<span id="TokenRing"></span><span id="tokenring"></span><span id="TOKENRING"></span>

**TokenRing** (15)


</dt> <dd></dd> <dt>

<span id="FDDI"></span><span id="fddi"></span>

" **F** " (16)


</dt> <dd></dd> <dt>

<span id="Infiniband"></span><span id="infiniband"></span><span id="INFINIBAND"></span>

**InfiniBand** (17)


</dt> <dd></dd> <dt>

<span id="Fibre_Channel"></span><span id="fibre_channel"></span><span id="FIBRE_CHANNEL"></span>

**Fibre Channel** (18)


</dt> <dd></dd> <dt>

<span id="ISDN_BRI_Endpoint"></span><span id="isdn_bri_endpoint"></span><span id="ISDN_BRI_ENDPOINT"></span>

**ISDN BRI-Endpunkt** (19)


</dt> <dd></dd> <dt>

<span id="ISDN_B_Channel_Endpoint"></span><span id="isdn_b_channel_endpoint"></span><span id="ISDN_B_CHANNEL_ENDPOINT"></span>

**ISDN-B-Kanal Endpunkt** (20)


</dt> <dd></dd> <dt>

<span id="ISDN_D_Channel_Endpoint"></span><span id="isdn_d_channel_endpoint"></span><span id="ISDN_D_CHANNEL_ENDPOINT"></span>

**ISDN-D-Kanal Endpunkt** (21)


</dt> <dd></dd> <dt>

<span id="IPv4_v6"></span><span id="ipv4_v6"></span><span id="IPV4_V6"></span>

**IPv4/V6** (22)


</dt> <dd></dd> <dt>

<span id="BGP"></span><span id="bgp"></span>

**BGP** (23)


</dt> <dd></dd> <dt>

<span id="OSPF"></span><span id="ospf"></span>

**OSPF** (24)


</dt> <dd></dd> <dt>

<span id="MPLS"></span><span id="mpls"></span>

**MPLS** (25)


</dt> <dd></dd> <dt>

<span id="UDP"></span><span id="udp"></span>

**UDP** (26)


</dt> <dd></dd> <dt>

<span id="TCP"></span><span id="tcp"></span>

**TCP** (27)


</dt> <dd></dd> </dl>

</dd> <dt>

**Timeoflaststatechange**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("timeoflaststatechange"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| if-MIB. iflatstchange ")
</dt> </dl>

Das Datum und die Uhrzeit der letzten Änderung der **enabledstate** -Eigenschaft. Wenn **enabledstate** nicht geändert wurde und diese Eigenschaft aufgefüllt ist, muss Sie auf einen Wert von 0 (null) festgelegt werden. Wenn eine Zustandsänderung angefordert, aber abgelehnt oder noch nicht verarbeitet wurde, darf die Eigenschaft nicht aktualisiert werden.

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

[**CIM \_ serviceaccesspoint**](cim-serviceaccesspoint.md)
</dt> </dl>

 

