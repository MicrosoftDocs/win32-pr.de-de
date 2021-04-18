---
title: Media. durationString
description: Die durationString-Eigenschaft ruft einen Zeichen folgen Wert ab, der die Dauer des aktuellen Medien Elements im hh mm ss-Format angibt.
ms.assetid: dfcb4c2e-c62c-4c3e-a9f4-fd147fb5b28c
keywords:
- Media. durationString-Windows-Media Player
topic_type:
- apiref
api_name:
- Media.durationString
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f1bbb89716ab1d06b176754396611ab22980659
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368689"
---
# <a name="mediadurationstring"></a>Media. durationString

Die **durationString** -Eigenschaft ruft einen **Zeichen** folgen Wert ab, der die Dauer des aktuellen Medien Elements im Format hh: mm: SS angibt.

## <a name="syntax"></a>Syntax

*Player*. *currentMedia*. **durationString**

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine schreibgeschützte **Zeichenfolge**.

## <a name="remarks"></a>Bemerkungen

, Wenn diese Eigenschaft mit einem anderen als dem in *Player* angegebenen Medien Element verwendet wird. **currentMedia** kann keinen gültigen Wert enthalten. Wenn das Medien Element weniger als eine Stunde lang ist, wird der HH:-Teil des Rückgabewerts ausgelassen.

Zum Abrufen des Werts dieser Eigenschaft ist Lesezugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).

## <a name="examples"></a>Beispiele

Im folgenden JScript-Beispiel werden *Medien* verwendet. **durationString** , um die Dauer des aktuellen Medien Elements als formatierten Text anzuzeigen. Ein HTML div-Element mit dem Namen MediaInfo zeigt die Dauer Informationen an. Das **Player** -Objekt wurde mit ID = "Player" erstellt.


```JScript
<!-- Create an event handler to update the display when
 the current media item changes. -->
<SCRIPT LANGUAGE = "JScript"  FOR = Player  EVENT = OpenStateChange(NewState)>

// Test whether the new media item is open.
if (NewState == 13){

   // Write the formatted duration string to the DIV region.
   MediaInfo.innerHTML = "Duration: " + Player.currentMedia.durationString;
}
</SCRIPT>

```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7,0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Medienobjekt**](media-object.md)
</dt> <dt>

[**Media. Duration**](media-duration.md)
</dt> <dt>

[**Player. currentMedia**](player-currentmedia.md)
</dt> <dt>

[**Settings. mediaaccessrights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestmediaaccessrights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





