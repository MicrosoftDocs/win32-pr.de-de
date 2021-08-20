---
description: Die SPFILENOTIFY \_ LANGMISMATCH-Benachrichtigung wird an die Rückrufroutine gesendet, wenn die Sprache der zu kopierenden Datei nicht mit der Sprache einer vorhandenen Zieldatei übereinstimmt.
ms.assetid: dff3969e-5847-4ad5-b7d4-237144bbe8e6
title: SPFILENOTIFY_LANGMISMATCH Meldung (Setupapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50cae8788e3ffac2de5cc7fc115b9363b8ad4591a0a4dd2447a3f86f735bec1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117964468"
---
# <a name="spfilenotify_langmismatch-message"></a>SPFILENOTIFY \_ LANGMISMATCH-Nachricht

Die **SPFILENOTIFY \_ LANGMISMATCH-Benachrichtigung** wird an die Rückrufroutine gesendet, wenn die Sprache der zu kopierenden Datei nicht mit der Sprache einer vorhandenen Zieldatei übereinstimmt. Sie kann mithilfe des OR-Operators mit [**SPFILENOTIFY \_ TARGETEXISTS**](spfilenotify-targetexists.md) und/oder [**SPFILENOTIFY \_ TARGETNEWER**](spfilenotify-targetnewer.md)allein oder kombiniert an die Rückrufroutine gesendet werden.


```C++
SPFILENOTIFY_LANGMISMATCH
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) LanguageInfo;
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Param1* 
</dt> <dd>

Zeiger auf eine [**FILEPATHS-Struktur,**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) die Informationen zu den Pfaden der Quell- und Zieldateien enthält.

</dd> <dt>

*Param2* 
</dt> <dd>

Identifiziert die nicht übereinstimmenden Sprachen. Dieser Member verfügt über den Sprachbezeichner der Quelldatei im unteren Wort und den Sprachbezeichner der vorhandenen Zieldatei im hohen Wort.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Rückrufroutine sollte einen der folgenden Werte zurückgeben.



| Rückgabecode                                                                          | Beschreibung                                                             |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <dt>**STIMMT**</dt> </dl>  | Kopieren Sie die Datei, und überschreiben Sie die vorhandene Datei.<br/>               |
| <dl> <dt>**FALSE**</dt> </dl> | Überspringen Sie den Kopiervorgang. Überschreiben Sie die vorhandene Datei nicht.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Setupapi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Übersicht](overview.md)
</dt> <dt>

[Benachrichtigungen](notifications.md)
</dt> <dt>

[**Filepaths**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> <dt>

[**SetupInstallFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea)
</dt> <dt>

[**SetupInstallFileEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa)
</dt> <dt>

[**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)
</dt> </dl>

 

 




