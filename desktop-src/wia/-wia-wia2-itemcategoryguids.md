---
description: Windows-Abbild Erfassungs Elemente (WIA) 2,0 sind in Kategorien unterteilt, die definieren, wie ein IWiaItem2 behandelt oder verwendet werden soll.
ms.assetid: 927f4957-aedf-4eef-8892-91cf9b56e1a2
title: WIA 2,0-Element Kategorie-GUIDs (wiadef. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_CATEGORY_AUTO
- WIA_CATEGORY_FEEDER
- WIA_CATEGORY_FEEDER_BACK
- WIA_CATEGORY_FEEDER_FRONT
- WIA_CATEGORY_FILM
- WIA_CATEGORY_FINISHED_FILE
- WIA_CATEGORY_FLATBED
- WIA_CATEGORY_FOLDER
- WIA_CATEGORY_ROOT
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: e2785d7d82e28641ebeefad730f02b3561a537a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348412"
---
# <a name="wia-20-item-category-guids"></a>WIA 2,0-Element Kategorie-GUIDs

Windows-Abbild Erfassungs Elemente (WIA) 2,0 sind in Kategorien unterteilt, die definieren, wie ein [**IWiaItem2**](-wia-iwiaitem2.md) behandelt oder verwendet werden soll. Wenn das Element z. b. einen feedvorgang darstellt, sollte die Anwendung erwarten, dass Sie die erforderlichen Eigenschaften für die Dokument feederstellung enthält und wie ein Dokument-feedvorgang funktioniert. Wenn das Element eine fertige Datei darstellt, sollte eine WIA 2,0-Anwendung diese auf diese Weise behandeln, wobei angenommen wird, dass die Daten statisch sind und sich auf dem Gerät befinden. (Die Regeln für jedes Element werden in den einzelnen Spezifikations Dokumenten definiert.) Jede Kategorie verfügt über eine GUID-typkonstante.



| Konstante                                                                                                                                                                                               | BESCHREIBUNG                                                                                                                                                                    |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WIA_CATEGORY_AUTO"></span><span id="wia_category_auto"></span><dl> <dt>**Automatische WIA- \_ Kategorie \_**</dt> </dl>                             | Ein Element, das die automatischen Konfigurationseinstellungen für ein WIA 2,0-Überprüfungs Gerät darstellt, das die automatisch konfigurierte Überprüfung unterstützt.<br/>                                   |
| <span id="WIA_CATEGORY_FEEDER"></span><span id="wia_category_feeder"></span><dl> <dt>**Kategorie- \_ \_ Feeder WIA**</dt> </dl>                       | Ein feedreement, bei dem es sich um eine programmierbare Datenquelle handelt und die Standardregeln und-Eigenschaften Sätze befolgt, die zur Unterstützung von Dokumenten<br/>                             |
| <span id="WIA_CATEGORY_FEEDER_BACK"></span><span id="wia_category_feeder_back"></span><dl> <dt>**Zurücksetzen \_ der \_ Kategorie \_**</dt> </dl>       | Eine programmierbare Datenquelle, die die Back-End-Datenquelle eines Duplex-Basis-feederelements beschreibt.<br/>                                                                       |
| <span id="WIA_CATEGORY_FEEDER_FRONT"></span><span id="wia_category_feeder_front"></span><dl> <dt>**\_ \_ \_ Vorschub**</dt> </dl>    | Eine programmierbare Datenquelle, die die Datenquelle auf der Vorderseite eines Duplex-Basis-feederelements beschreibt.<br/>                                                                      |
| <span id="WIA_CATEGORY_FILM"></span><span id="wia_category_film"></span><dl> <dt>**Film der Kategorie "WIA" \_ \_**</dt> </dl>                             | Ein Film Element, bei dem es sich um eine programmierbare Datenquelle handelt und die Standardregeln und-Eigenschaften Sätze befolgt, die für die Unterstützung von Einheiten zur<br/>                            |
| <span id="WIA_CATEGORY_FINISHED_FILE"></span><span id="wia_category_finished_file"></span><dl> <dt>**Datei der WIA- \_ Kategorie \_ abgeschlossen \_**</dt> </dl> | Ein Element, das keine programmierbare Datenquelle ist, oder ein Element, das Daten in einem fertigen Dateiformat bereitstellt, oder ein Ordner Element, das fertige Dateiformat Elemente enthält.<br/> |
| <span id="WIA_CATEGORY_FLATBED"></span><span id="wia_category_flatbed"></span><dl> <dt>**WIA- \_ Kategorie \_**</dt> </dl>                    | Ein Element, das eine programmierbare Datenquelle ist und den Standardregeln und-Eigenschafts Sätzen folgt, die zur Unterstützung von pllans-Scanvorgängen erforderlich sind.<br/>                     |
| <span id="WIA_CATEGORY_FOLDER"></span><span id="wia_category_folder"></span><dl> <dt>**Ordner "WIA \_ Category" \_**</dt> </dl>                       | Ein Ordner Speicher Element (keine programmierbare Datenquelle), das andere Ordner Elemente oder abgeschlossene Dateien oder beides enthält.<br/>                                                     |
| <span id="WIA_CATEGORY_ROOT"></span><span id="wia_category_root"></span><dl> <dt>**WIA \_ - \_ kategorienroot**</dt> </dl>                             | Das Stamm Element für das Gerät. <br/>                                                                                                                                      |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Wiadef. h</dt> </dl> |



 

 




