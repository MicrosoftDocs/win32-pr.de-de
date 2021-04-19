---
description: Die spfilenotify \_ langmismatch-Benachrichtigung wird an die Rückruf Routine gesendet, wenn die Sprache der zu kopierenden Datei nicht mit der Sprache einer vorhandenen Zieldatei übereinstimmt.
ms.assetid: dff3969e-5847-4ad5-b7d4-237144bbe8e6
title: SPFILENOTIFY_LANGMISMATCH Meldung (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3d7828c90dd4dabb8e1cb73a8dcca7ae33ebd3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359540"
---
# <a name="spfilenotify_langmismatch-message"></a>Spfilenotify \_ langmismatch-Meldung

Die **spfilenotify \_ langmismatch** -Benachrichtigung wird an die Rückruf Routine gesendet, wenn die Sprache der zu kopierenden Datei nicht mit der Sprache einer vorhandenen Zieldatei übereinstimmt. Sie kann mithilfe des OR-Operators, mit [**spfilenotify \_ targetexists**](spfilenotify-targetexists.md) und/oder [**spfilenotify \_ targetneueren**](spfilenotify-targetnewer.md), einzeln oder in Kombination mit der Rückruf Routine gesendet werden.


```C++
SPFILENOTIFY_LANGMISMATCH
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) LanguageInfo;
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Param1* 
</dt> <dd>

Zeiger auf eine [**FilePath**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) -Struktur, die Informationen zu den Pfaden der Quell-und Zieldateien enthält.

</dd> <dt>

*Param2* 
</dt> <dd>

Identifiziert die nicht übereinstimmenden Sprachen. Dieser Member hat den sprach Bezeichner der Quelldatei im niedrigen Wort und den sprach Bezeichner der vorhandenen Zieldatei im hohen Wort.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Rückruf Routine muss einen der folgenden Werte zurückgeben.



| Rückgabecode                                                                          | Beschreibung                                                             |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <dt>**Fall**</dt> </dl>  | Kopieren Sie die Datei, und überschreiben Sie die vorhandene Datei.<br/>               |
| <dl> <dt>**Alarm**</dt> </dl> | Überspringen Sie den Kopiervorgang. Überschreiben Sie die vorhandene Datei nicht.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Setupapi. h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Übersicht](overview.md)
</dt> <dt>

[Benachrichtigungen](notifications.md)
</dt> <dt>

[**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[**Setupcommitfilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[**Setupdefaultqueuecallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> <dt>

[**Setupinstallfile**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea)
</dt> <dt>

[**Setupinstallfileex**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa)
</dt> <dt>

[**Setupinstallfrominf-Abschnitt**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)
</dt> </dl>

 

 




