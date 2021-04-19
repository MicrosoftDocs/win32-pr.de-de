---
description: Die spfilenotify \_ fileincabinet-Benachrichtigung wird von setupiteratecabinet für jede Datei in der CAB-Datei an eine Rückruf Routine gesendet. Die Rückruf Routine muss einen Wert zurückgeben, der angibt, ob die Datei extrahiert werden soll.
ms.assetid: c6d89759-c0d4-4741-b992-43eaa0dc4f01
title: SPFILENOTIFY_FILEINCABINET Meldung (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 496db3cef814f2bf366f4cb6f91132efe01a2406
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357053"
---
# <a name="spfilenotify_fileincabinet-message"></a>Spfilenotify \_ fileincabinet-Nachricht

Die **spfilenotify \_ fileincabinet** -Benachrichtigung wird von [**setupiteratecabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) für jede Datei in der CAB-Datei an eine Rückruf Routine gesendet. Die Rückruf Routine muss einen Wert zurückgeben, der angibt, ob die Datei extrahiert werden soll.


```C++
SPFILENOTIFY_FILEINCABINET
  Param1 = (UINT) FileInCabinetInfo;
  Param2 = (UINT) CabinetFile;
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Param1* 
</dt> <dd>

Zeiger auf eine [**Datei \_ in \_ \_**](/windows/desktop/api/Setupapi/ns-setupapi-file_in_cabinet_info_a) der CAB-Info-Struktur, die Informationen über die Datei in der CAB-Datei enthält.

</dd> <dt>

*Param2* 
</dt> <dd>

Zeiger auf eine mit NULL endenden Zeichenfolge, die den Dateinamen der CAB-Datei enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Rückruf Routine sollte eine der folgenden zurückgeben.



| Rückgabecode                                                                                 | Beschreibung                                  |
|---------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**fileOp-über \_ springen**</dt> </dl> | Extrahieren Sie die Datei nicht, und überspringen Sie Sie.<br/> |
| <dl> <dt>**fileOp- \_ doit**</dt> </dl> | Entpacken Sie die Datei.<br/>                 |



 

Wenn Ihre Rückruf Routine fileOp \_ doit zurückgibt, sollte der Name, der für die extrahierte Datei verwendet werden soll, im **fulltargetname** -Member der [**Datei in der CAB \_ \_ \_ Info**](/windows/desktop/api/Setupapi/ns-setupapi-file_in_cabinet_info_a) -Struktur angegeben werden, die an die Routine in *param1* übergeben wird.

> [!Note]  
> Es ist keine standardmäßige CAB-Rückruf Routine vorhanden. Die Setup Anwendung sollte eine Rückruf Routine bereitstellen, um die von [**setupiteratecabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta)gesendeten Benachrichtigungen zu verarbeiten.

 

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

[**Datei \_ in CAB- \_ \_ Info**](/windows/desktop/api/Setupapi/ns-setupapi-file_in_cabinet_info_a)
</dt> <dt>

[**Setupiteratecabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta)
</dt> </dl>

 

 




