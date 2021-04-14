---
title: Ibackgroundcopyerror-Schnittstelle (deliveryoptimization. h)
description: Verwenden Sie die ibackgroundcopyerror-Schnittstelle, um die Ursache eines Fehlers zu ermitteln, und, wenn der Übertragungsprozess fortgesetzt werden kann.
ms.assetid: 7DCB63CF-4180-4DC3-9093-07C4F8CF7A8E
keywords:
- Ibackgroundcopyerror-Schnittstelle
- Ibackgroundcopyerror-Schnittstelle, beschrieben
topic_type:
- apiref
api_name:
- IBackgroundCopyError
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1f35365d56ce9391a746e479e1b59034342ebf62
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476371"
---
# <a name="ibackgroundcopyerror-interface"></a>Ibackgroundcopyerror-Schnittstelle

Verwenden Sie die **ibackgroundcopyerror** -Schnittstelle, um die Ursache eines Fehlers zu ermitteln, und, wenn der Übertragungsprozess fortgesetzt werden kann.

Erstellt nur dann ein Fehler Objekt, wenn der Status des Auftrags BG_JOB_STATE_ERROR oder BG_JOB_STATE_TRANSIENT_ERROR ist. Erstellt kein Fehler Objekt, wenn eine **ibackgroundcopyxxxx** -Schnittstellen Methode fehlschlägt. Das Error-Objekt ist verfügbar, bis die Daten übertragen werden (der Status des Auftrags ändert sich in BG_JOB_STATE_TRANSFERRING) für den Auftrag.

Zum Abrufen eines **ibackgroundcopyerror** -Objekts müssen Sie die [**ibackgroundcopyjob:: getError**](ibackgroundcopyjob-geterror.md) -Methode aufrufen.

## <a name="members"></a>Member

Die **ibackgroundcopyerror** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Ibackgroundcopyerror** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ibackgroundcopyerror** -Schnittstelle verfügt über diese Methoden.



| Methode                                                   | BESCHREIBUNG                                                                                 |
|:---------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [**GetError**](ibackgroundcopyerror-geterror-method.md) | Ruft den Fehlercode ab und identifiziert den Kontext, in dem der Fehler aufgetreten ist.<br/> |
| [**GetFile**](ibackgroundcopyerror-getfile-method.md)   | Ruft einen Schnittstellen Zeiger auf das File-Objekt ab, das dem Fehler zugeordnet ist.<br/>     |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1709, \[ nur Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, Version 1709, \[ nur Desktop-Apps\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Deliveryoptimization. idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyError ist als 19c613a0-fcb8-4f 28-81ae-897c3d078-Datei definiert.<br/>             |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**BG_JOB_STATE**](bg-job-state-.md)
</dt> <dt>

[**Ibackgroundcopyjob:: getError**](ibackgroundcopyjob-geterror.md)
</dt> <dt>

[**Ibackgroundcopyjob:: GetState**](ibackgroundcopyjob-getstate.md)
</dt> <dt>

[**Ibackgroundcopycallback:: joberror**](ibackgroundcopycallback-joberror-method.md)
</dt> </dl>

 

