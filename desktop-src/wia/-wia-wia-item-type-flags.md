---
description: Die folgenden Konstanten geben den Windows-Abbild Erfassungs Element-Elementtyp (WIA) an.
ms.assetid: 7961f692-088a-4f3b-84e9-5fabb0373c3c
title: WIA-Elementtyp-Flags (wiadef. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WiaItemTypeAnalyze
- WiaItemTypeAudio
- WiaItemTypeBurst
- WiaItemTypeDeleted
- WiaItemTypeDevice
- WiaItemTypeDisconnected
- WiaItemTypeDocument
- WiaItemTypeFile
- WiaItemTypeFolder
- WiaItemTypeFree
- WiaItemTypeGenerated
- WiaItemTypeHasAttachments
- WiaItemTypeHPanorama
- WiaItemTypeImage
- WiaItemTypeProgrammableDataSource
- WiaItemTypeRemoved
- WiaItemTypeRoot
- WiaItemTypeStorage
- WiaItemTypeTransfer
- WiaItemTypeTwainCapabilityPassThrough
- WiaItemTypeVideo
- WiaItemTypeVPanorama
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: c5b7a9e6108825205b2d8bc5ab40ce8096e32ebd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345734"
---
# <a name="wia-item-type-flags"></a>WIA-Elementtyp-Flags

Die folgenden Konstanten geben den Windows-Abbild Erfassungs Element-Elementtyp (WIA) an.



| Konstante                                                                                                                                                                                                                                                                                     | BESCHREIBUNG                                                                                                                                                                                                                                                                                       |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WiaItemTypeAnalyze"></span><span id="wiaitemtypeanalyze"></span><span id="WIAITEMTYPEANALYZE"></span><dl> <dt>**Wiaitemtypeanalysis**</dt> </dl>                                                                             | Dieses Element unterstützt die [**iwiaitem:: analyzeitem**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-analyzeitem) -Methode. *Diese Konstante wird von nicht unterstützt* . Windows Vista *und höher.*<br/>                                                                                                                               |
| <span id="WiaItemTypeAudio"></span><span id="wiaitemtypeaudio"></span><span id="WIAITEMTYPEAUDIO"></span><dl> <dt>**Wiaitemtypeaudiodatei**</dt> </dl>                                                                                     | Das Element ist eine Audiodatei. Nur gültig für Elemente, die auch über das **wiaitemtypefile** -Attribut verfügen. <br/>                                                                                                                                                                                     |
| <span id="WiaItemTypeBurst"></span><span id="wiaitemtypeburst"></span><span id="WIAITEMTYPEBURST"></span><dl> <dt>**Wiaitemtypeburst**</dt> </dl>                                                                                     | Nur für Ordner. Die Bilder in diesem Ordner wurden in einer kontinuierlichen Zeitsequenz entnommen. *Diese Konstante wird von nicht unterstützt* . Windows Vista *und höher.*<br/>                                                                                                                                       |
| <span id="WiaItemTypeDeleted"></span><span id="wiaitemtypedeleted"></span><span id="WIAITEMTYPEDELETED"></span><dl> <dt>**Wiaitemtypedeleted**</dt> </dl>                                                                             | Das Element ist in der Struktur als gelöscht markiert. <br/>                                                                                                                                                                                                                                          |
| <span id="WiaItemTypeDevice"></span><span id="wiaitemtypedevice"></span><span id="WIAITEMTYPEDEVICE"></span><dl> <dt>**Wiaitemtypedevice**</dt> </dl>                                                                                 | Das Element stellt ein verbundenes Gerät dar. <br/>                                                                                                                                                                                                                                               |
| <span id="WiaItemTypeDisconnected"></span><span id="wiaitemtypedisconnected"></span><span id="WIAITEMTYPEDISCONNECTED"></span><dl> <dt>**Wiaitemtypegetrennte**</dt> </dl>                                                         | Das Element stellt ein nicht verbundenes Gerät dar. <br/>                                                                                                                                                                                                                                            |
| <span id="WiaItemTypeDocument"></span><span id="wiaitemtypedocument"></span><span id="WIAITEMTYPEDOCUMENT"></span><dl> <dt>**Wiaitemtypedocument**</dt> </dl>                                                                         | Das Element stellt ein Dokument dar. *Diese Konstante wird nur von* Windows Vista *und höher.*<br/>                                                                                                                                                                                        |
| <span id="WiaItemTypeFile"></span><span id="wiaitemtypefile"></span><span id="WIAITEMTYPEFILE"></span><dl> <dt>**Wiaitemtypefile**</dt> </dl>                                                                                         | Das Element ist eine Datei. <br/>                                                                                                                                                                                                                                                                   |
| <span id="WiaItemTypeFolder"></span><span id="wiaitemtypefolder"></span><span id="WIAITEMTYPEFOLDER"></span><dl> <dt>**Wiaitemtypefolder**</dt> </dl>                                                                                 | Das Element ist ein Ordner. <br/>                                                                                                                                                                                                                                                                 |
| <span id="WiaItemTypeFree"></span><span id="wiaitemtypefree"></span><span id="WIAITEMTYPEFREE"></span><dl> <dt>**Wiaitemtypefree**</dt> </dl>                                                                                         | Das Element ist nicht initialisiert oder wurde gelöscht. <br/>                                                                                                                                                                                                                                        |
| <span id="WiaItemTypeGenerated"></span><span id="wiaitemtypegenerated"></span><span id="WIAITEMTYPEGENERATED"></span><dl> <dt>**Wiaitemtypegenerated**</dt> </dl>                                                                     | Dieses Element wurde von der Anwendung oder dem Treiber erstellt und verfügt nicht über ein entsprechendes Element in der Treiber Elementstruktur. <br/>                                                                                                                                                               |
| <span id="WiaItemTypeHasAttachments"></span><span id="wiaitemtypehasattachments"></span><span id="WIAITEMTYPEHASATTACHMENTS"></span><dl> <dt>**Wiaitemtypehasattachments**</dt> </dl>                                                 | Das Element verfügt über Dateianhänge. *Diese Konstante wird von nicht unterstützt* . Windows Vista *und höher.*<br/>                                                                                                                                                                                          |
| <span id="WiaItemTypeHPanorama"></span><span id="wiaitemtypehpanorama"></span><span id="WIAITEMTYPEHPANORAMA"></span><dl> <dt>**Wiaitemtypehpanorama**</dt> </dl>                                                                     | Das Element stellt ein horizontales Panoramabild dar. *Diese Konstante wird von nicht unterstützt* . Windows Vista *und höher.*<br/>                                                                                                                                                                       |
| <span id="WiaItemTypeImage"></span><span id="wiaitemtypeimage"></span><span id="WIAITEMTYPEIMAGE"></span><dl> <dt>**Wiaitemtypeimage**</dt> </dl>                                                                                     | Das Element ist eine Bilddatei. Nur gültig für Elemente, die auch über das **wiaitemtypefile** -Attribut verfügen. <br/>                                                                                                                                                                                     |
| <span id="WiaItemTypeProgrammableDataSource"></span><span id="wiaitemtypeprogrammabledatasource"></span><span id="WIAITEMTYPEPROGRAMMABLEDATASOURCE"></span><dl> <dt>**Wiaitemtypeprogrammabledatasource**</dt> </dl>                 | Das Element stellt eine programmierbare Datenquelle dar. *Diese Konstante wird nur von* Windows Vista *und höher.*<br/>                                                                                                                                                                        |
| <span id="WiaItemTypeRemoved"></span><span id="wiaitemtyperemoved"></span><span id="WIAITEMTYPEREMOVED"></span><dl> <dt>**Wiaitemtyperemoved**</dt> </dl>                                                                             | Das Element wurde vom Gerät entfernt. <br/>                                                                                                                                                                                                                                            |
| <span id="WiaItemTypeRoot"></span><span id="wiaitemtyperoot"></span><span id="WIAITEMTYPEROOT"></span><dl> <dt>**Wiaitemtyperoot**</dt> </dl>                                                                                         | Identifiziert das Stamm Element in der Struktur von Element Objekten des Geräts. *Diese Konstante wird nur von* Windows Vista *und höher.*<br/>                                                                                                                                                         |
| <span id="WiaItemTypeStorage"></span><span id="wiaitemtypestorage"></span><span id="WIAITEMTYPESTORAGE"></span><dl> <dt>**Wiaitemtypestorage**</dt> </dl>                                                                             | Das Element stellt ein Speichermedium dar. <br/>                                                                                                                                                                                                                                                 |
| <span id="WiaItemTypeTransfer"></span><span id="wiaitemtypetransfer"></span><span id="WIAITEMTYPETRANSFER"></span><dl> <dt>**Wiaitemtypetransfer**</dt> </dl>                                                                         | Das Element kann übertragen werden. <br/>                                                                                                                                                                                                                                                          |
| <span id="WiaItemTypeTwainCapabilityPassThrough"></span><span id="wiaitemtypetwaincapabilitypassthrough"></span><span id="WIAITEMTYPETWAINCAPABILITYPASSTHROUGH"></span><dl> <dt>**Wiaitemtypetwaincapabilitypassthrough**</dt> </dl> | Dieser Typ gibt an, dass das WIA-Gerät die TWAIN-Funktionsdaten von der TWAIN-Kompatibilitätsschicht empfangen kann. Wenn dieser Typ festgelegt ist, wird jede TWAIN-Funktion, die während einer TWAIN-Sitzung nicht von der TWAIN-Kompatibilitätsschicht verstanden wird, an den WIA-Treiber übermittelt. <br/> |
| <span id="WiaItemTypeVideo"></span><span id="wiaitemtypevideo"></span><span id="WIAITEMTYPEVIDEO"></span><dl> <dt>**Wiaitemtypevideo**</dt> </dl>                                                                                     | Das Element stellt Streaming-Video dar. *Diese Konstante wird von keinem der folgenden Werte unterstützt* : Windows Server 2003 *,* Windows Vista *oder höher.*<br/>                                                                                                                                                      |
| <span id="WiaItemTypeVPanorama"></span><span id="wiaitemtypevpanorama"></span><span id="WIAITEMTYPEVPANORAMA"></span><dl> <dt>**Wiaitemtypevpanorama**</dt> </dl>                                                                     | Das Element stellt ein vertikales Panoramabild dar. *Diese Konstante wird von nicht unterstützt* . Windows Vista *und höher.*<br/>                                                                                                                                                                         |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, Windows XP \[ Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Wiadef. h</dt> </dl> |



 

 




