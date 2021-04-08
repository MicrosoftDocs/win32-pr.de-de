---
description: Die selectdefaultsubpicturelanguage-Methode legt die aktuelle Standardsprache des unter Bilds im mswebdvd-Objekt fest.
ms.assetid: e83980d1-c7cd-4755-9a27-3b0c2548009e
title: Selectdefaultsubpicturelanguage-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9d7dd4d66ae9d0580bf863ede9fff1e51d373e2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746248"
---
# <a name="selectdefaultsubpicturelanguage-method"></a>Selectdefaultsubpicturelanguage-Methode

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die- `SelectDefaultSubpictureLanguage` Methode legt die aktuelle Standardsprache des unter Bilds im **mswebdvd** -Objekt fest.

``` syntax
MSWebDVD.SelectDefaultSubpictureLanguage(iLang,iExt)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="iLang"></span><span id="ilang"></span><span id="ILANG"></span>*ilang*
</dt> <dd>

Gibt die Sprache als Ganzzahl an.

</dd> <dt>

<span id="iExt"></span><span id="iext"></span><span id="IEXT"></span>*iext*
</dt> <dd>

Gibt die unter Bild Spracherweiterung als Ganzzahl an.



| Wert | BESCHREIBUNG                    |
|-------|--------------------------------|
| 0     | Erweiterung nicht angegeben        |
| 1     | Normale Beschriftungen                |
| 2     | Große Beschriftungen                   |
| 3     | Untergeordnete Beschriftungen            |
| 5     | Normale Untertitel         |
| 6     | Big Closed-Beschriftungen            |
| 7     | Untertitel der untergeordneten Elemente     |
| 9     | Erzwungen                         |
| 13    | Kommentare des normalen Direktors     |
| 14    | Kommentare zu Big Director        |
| 15    | Die Kommentare der untergeordneten Elemente |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Die unter Bilder-Spracherweiterung bietet weitere Informationen über das untergeordnete Bild.

 

 



