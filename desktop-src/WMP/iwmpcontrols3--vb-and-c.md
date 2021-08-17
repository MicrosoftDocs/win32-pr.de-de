---
title: IWMPControls3-Schnittstelle (VB und C) (Wmp.h)
description: Stellt Eigenschaften und Methoden für die Auswahl der Audiosprache sowie Unterstützung bereit, die die IWMPControls2-Schnittstelle ergänzen. Zusätzlich zu den Eigenschaften und Methoden, die von IWMPControls2 geerbt wurden, macht die IWMPControls3-Schnittstelle die folgenden Eigenschaften verfügbar.
ms.assetid: 1f42a352-da97-4382-9b59-a9b074aa2a5a
keywords:
- IWMPControls3-Schnittstelle (VB und C) Windows Media Player
- IWMPControls3-Schnittstelle (VB und C) Windows Media Player beschrieben
topic_type:
- apiref
api_name:
- IWMPControls3 (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2baf3f0b5f2bc4f2e4d0bfa5ccddd717c913aa30f5e24b5559eb527c910bcaf7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135413"
---
# <a name="iwmpcontrols3-vb-and-c-interface"></a>IWMPControls3-Schnittstelle (VB und C#)

Stellt Eigenschaften und Methoden für die Auswahl der Audiosprache sowie Unterstützung bereit, die die **IWMPControls2-Schnittstelle** ergänzen.

Zusätzlich zu den Eigenschaften und Methoden, die von **IWMPControls2** geerbt wurden, macht die **IWMPControls3-Schnittstelle** die folgenden Eigenschaften verfügbar.

## <a name="members"></a>Member

Die **IWMPControls3-Schnittstelle (VB und C#)** verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **IWMPControls3-Schnittstelle (VB und C#)** verfügt über diese Methoden.



| Methode                                                                                                         | Beschreibung                                                                                               |
|:---------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| [**getAudioLanguageDescription**](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguagedescription--vb-and-c.md) | Gibt die Beschreibung für die Audiosprache zurück, die dem angegebenen einbasierten Index entspricht.<br/> |
| [**getAudioLanguageID**](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguageid--vb-and-c.md)                   | Gibt die LCID für einen angegebenen Audiosprachindex zurück.<br/>                                         |
| [**getLanguageName**](wmplibiwmpcontrols3-iwmpcontrols3-getlanguagename--vb-and-c.md)                         | Gibt den Namen der Audiosprache mit der angegebenen LCID zurück.<br/>                                |



 

### <a name="properties"></a>Eigenschaften

Die **IWMPControls3-Schnittstelle (VB und C#)** verfügt über diese Eigenschaften.



| Eigenschaft                                                                                                              | Zugriffstyp           | Beschreibung                                                                                                                                         |
|:----------------------------------------------------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**audioLanguageCount**](wmplibiwmpcontrols3-iwmpcontrols3-audiolanguagecount--vb-and-c.md)<br/>               | Schreibgeschützt<br/>  | Ruft die Anzahl der unterstützten Audiosprachen ab. <br/>                                                                                            |
| [**currentAudioLanguage**](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)<br/>           | Lesen/Schreiben<br/> | Ruft den Gebietsschemabezeichner (LCID) der Audiosprache für die Wiedergabe ab oder legt diese fest. <br/>                                                           |
| [**currentAudioLanguageIndex**](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguageindex--vb-and-c.md)<br/> | Lesen/Schreiben<br/> | Ruft den einbasierten Index ab, der der Audiosprache für die Wiedergabe entspricht, oder legt diesen fest. <br/>                                                   |
| [**currentPositionTimecode**](wmplibiwmpcontrols3-iwmpcontrols3-currentpositiontimecode--vb-and-c.md)<br/>     | Lesen/Schreiben<br/> | Ruft die aktuelle Position im aktuellen Medienelement mithilfe eines Zeitcodeformats ab oder legt diese fest. Diese Eigenschaft unterstützt derzeit SMPTE-Zeitcode. <br/> |



 

Abrufen einer **IWMPControls3-Schnittstelle** durch Umwandeln des werts, der von der [**AxWindowsMediaPlayer.Ctlcontrols-Eigenschaft**](axwmplib-axwindowsmediaplayer-ctlcontrols--vb-and-c.md) zurückgegeben wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmp.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Schnittstellen für Visual Basic .NET und C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**IWMPControls-Schnittstelle (VB und C#)**](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[**IWMPControls2-Schnittstelle (VB und C#)**](iwmpcontrols2--vb-and-c.md)
</dt> </dl>

 

 





