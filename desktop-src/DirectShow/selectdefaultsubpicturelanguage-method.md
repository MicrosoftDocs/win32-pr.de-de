---
description: Die SelectDefaultSubpictureLanguage-Methode legt die aktuelle Standardunterbildsprache im MSWebDVD-Objekt fest.
ms.assetid: e83980d1-c7cd-4755-9a27-3b0c2548009e
title: SelectDefaultSubpictureLanguage-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3aaa6b927d33626299258ac54136e1a67b0dedb40427a35d9c79465be3e9a15d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072584"
---
# <a name="selectdefaultsubpicturelanguage-method"></a>SelectDefaultSubpictureLanguage-Methode

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die `SelectDefaultSubpictureLanguage` -Methode legt die aktuelle Standardunterbildsprache im **MSWebDVD-Objekt** fest.

``` syntax
MSWebDVD.SelectDefaultSubpictureLanguage(iLang,iExt)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="iLang"></span><span id="ilang"></span><span id="ILANG"></span>*Ilang*
</dt> <dd>

Gibt die Sprache als ganze Zahl an.

</dd> <dt>

<span id="iExt"></span><span id="iext"></span><span id="IEXT"></span>*iExt*
</dt> <dd>

Gibt die Untergeordnete Spracherweiterung als Ganze Zahl an.



| Wert | Beschreibung                    |
|-------|--------------------------------|
| 0     | Erweiterung nicht angegeben        |
| 1     | Normale Beschriftungen                |
| 2     | Große Beschriftungen                   |
| 3     | Beschriftungen für untergeordnete Elemente            |
| 5     | Normale Untertitel         |
| 6     | Große Untertitel            |
| 7     | Untertitel für untergeordnete Elemente     |
| 9     | Erzwungen                         |
| 13    | Kommentare zu normalen Verzeichnissen     |
| 14    | Big Director es Comments (Kommentare von Big Director)        |
| 15    | Children es Director es Comments |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Die Spracherweiterung subpicture enthält weitere Informationen zur Unterbildsprache.

 

 



