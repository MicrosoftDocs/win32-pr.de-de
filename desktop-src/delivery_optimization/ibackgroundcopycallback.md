---
title: Ibackgroundcopycallback-Schnittstelle (deliveryoptimization. h)
description: Implementieren Sie die ibackgroundcopycallback-Schnittstelle, um eine Benachrichtigung zu erhalten, dass ein Auftrag abgeschlossen ist, geändert wurde oder fehlerhaft ist. Clients verwenden diese Schnittstelle, anstatt den Status des Auftrags abzufragen.
ms.assetid: CF85D852-1B4E-4BC2-B6A6-0035ED3C439C
keywords:
- Ibackgroundcopycallback-Schnittstelle
- Ibackgroundcopycallback-Schnittstelle, beschrieben
topic_type:
- apiref
api_name:
- IBackgroundCopyCallback
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4169acec87e4d1e8a31eecaa4f93b9404aafb714
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340326"
---
# <a name="ibackgroundcopycallback-interface"></a>Ibackgroundcopycallback-Schnittstelle

Implementieren Sie die **ibackgroundcopycallback** -Schnittstelle, um eine Benachrichtigung zu erhalten, dass ein Auftrag abgeschlossen ist, geändert wurde oder fehlerhaft ist. Clients verwenden diese Schnittstelle, anstatt den Status des Auftrags abzufragen.

## <a name="members"></a>Member

Die **ibackgroundcopycallback** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Ibackgroundcopycallback** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ibackgroundcopycallback** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                    | BESCHREIBUNG                                                                       |
|:--------------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| [**Joberror**](ibackgroundcopycallback-joberror-method.md)               | Wird aufgerufen, wenn ein Fehler auftritt.<br/>                                           |
| [**Jobmodifizierung**](ibackgroundcopycallback-jobmodification-method.md) | Wird aufgerufen, wenn ein Auftrag geändert wird.<br/>                                         |
| [**Jobübertragene**](ibackgroundcopycallback-jobtransferred.md)          | Wird aufgerufen, wenn alle Dateien im Auftrag erfolgreich übertragen wurden.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Um Benachrichtigungen zu empfangen, rufen Sie die [**ibackgroundcopyjob:: setnotifyinterface**](ibackgroundcopyjob-setnotifyinterface.md) -Methode auf, um den Schnittstellen Zeiger auf die **ibackgroundcopycallback** -Implementierung anzugeben. Um anzugeben, welche Benachrichtigungen Sie empfangen möchten, müssen Sie die [**ibackgroundcopyjob:: setnotifyflags**](ibackgroundcopyjob-setnotifyflags.md) -Methode aufrufen.

Ruft ihre Rückrufe auf, solange der Schnittstellen Zeiger gültig ist. Die Benachrichtigungs Schnittstelle ist nicht mehr gültig, wenn die Anwendung beendet wird. Behält die Benachrichtigungs Schnittstelle nicht bei. Folglich sollte der Initialisierungs Prozess ihrer Anwendung die [**setnotifyinterface**](ibackgroundcopyjob-setnotifyinterface.md) -Methode für die vorhandenen Aufträge aufrufen, für die Sie eine Benachrichtigung erhalten möchten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1709, \[ nur Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, Version 1709, \[ nur Desktop-Apps\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Deliveryoptimization. idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyCallback ist als 97ea99c7-0186-4ad4-8df9-c5b4e0ed6b22 definiert.<br/>          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IBackgroundCopyJob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**Ibackgroundcopyjob:: setnotifyflags**](ibackgroundcopyjob-setnotifyflags.md)
</dt> <dt>

[**Ibackgroundcopyjob:: setnotifyinterface**](ibackgroundcopyjob-setnotifyinterface.md)
</dt> </dl>

 

