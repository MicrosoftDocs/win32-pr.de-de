---
description: Die SelectDefaultAudioLanguage-Methode legt die aktuelle Standardaudiosprache im MSWebDVD-Objekt fest.
ms.assetid: 7d63b7ef-2b03-4929-822a-c4d11fb7a825
title: SelectDefaultAudioLanguage-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4b649993cc3e110e78ba0a674e414dd4214af982dd44d64fcc1aca7646d1b04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072624"
---
# <a name="selectdefaultaudiolanguage-method"></a>SelectDefaultAudioLanguage-Methode

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die `SelectDefaultAudioLanguage` -Methode legt die aktuelle Standardaudiosprache im MSWebDVD-Objekt fest.

``` syntax
MSWebDVD.SelectDefaultAudioLanguage(iLang, iExt)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="iLang"></span><span id="ilang"></span><span id="ILANG"></span>*Ilang*
</dt> <dd>

Gibt die Sprache als Ganzzahl-LCID-Wert an.

</dd> <dt>

<span id="iExt"></span><span id="iext"></span><span id="IEXT"></span>*iExt*
</dt> <dd>

Gibt die DVD-Audiospracherweiterung als ganzzahligen Wert an.



| Wert | Beschreibung       |
|-------|-------------------|
| 0     | NotSpecified      |
| 1     | Untertitel          |
| 2     | VisuallyImpaired  |
| 3     | DirectorComments1 |
| 4     | DirectorComments2 |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[MSWebDVD-Objekt](mswebdvd-object.md)
</dt> </dl>

 

 



