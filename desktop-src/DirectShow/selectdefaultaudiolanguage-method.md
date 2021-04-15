---
description: Die selectdefaultaudiolanguage-Methode legt die aktuelle Standard Audiosprache im mswebdvd-Objekt fest.
ms.assetid: 7d63b7ef-2b03-4929-822a-c4d11fb7a825
title: Selectdefaultaudiolanguage-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 126de6daf4f5e0337058495a3ee7898594bfd704
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521275"
---
# <a name="selectdefaultaudiolanguage-method"></a>Selectdefaultaudiolanguage-Methode

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die `SelectDefaultAudioLanguage` -Methode legt die aktuelle Standard Audiosprache im mswebdvd-Objekt fest.

``` syntax
MSWebDVD.SelectDefaultAudioLanguage(iLang, iExt)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="iLang"></span><span id="ilang"></span><span id="ILANG"></span>*ilang*
</dt> <dd>

Gibt die Sprache als einen LCID-ganzzahligen Wert an.

</dd> <dt>

<span id="iExt"></span><span id="iext"></span><span id="IEXT"></span>*iext*
</dt> <dd>

Gibt die DVD-Audiosprach Erweiterung als ganzzahligen Wert an.



| Wert | BESCHREIBUNG       |
|-------|-------------------|
| 0     | NotSpecified      |
| 1     | Untertitel          |
| 2     | Visualisierungen beeinträchtigt  |
| 3     | DirectorComments1 |
| 4     | DirectorComments2 |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mswebdvd-Objekt](mswebdvd-object.md)
</dt> </dl>

 

 



