---
title: IBackgroundCopyFile2-Schnittstelle (deliveryoptimization. h)
description: Geben Sie mit der IBackgroundCopyFile2-Schnittstelle einen neuen Remote Namen für die Datei an, und rufen Sie die Liste der herunter zuladenden Bereiche ab.
ms.assetid: 28233310-9F2A-4567-B0B1-B549F862F3C8
keywords:
- IBackgroundCopyFile2-Schnittstelle
- IBackgroundCopyFile2-Schnittstelle, beschrieben
topic_type:
- apiref
api_name:
- IBackgroundCopyFile2
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4a866c8f18ee1dfb57f32ac3b2b9999e10106522
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040520"
---
# <a name="ibackgroundcopyfile2-interface"></a>IBackgroundCopyFile2-Schnittstelle

Geben Sie mit der **IBackgroundCopyFile2** -Schnittstelle einen neuen Remote Namen für die Datei an, und rufen Sie die Liste der herunter zuladenden Bereiche ab.

Die **IBackgroundCopyFile2** -Schnittstelle erbt von der [**ibackgroundcopyfile**](ibackgroundcopyfile.md) -Schnittstelle.

Um einen **IBackgroundCopyFile2** -Schnittstellen Zeiger abzurufen, verwenden Sie die **ibackgroundcopyfile:: QueryInterface** -Methode mithilfe __uuidof (IBackgroundCopyFile2) für den Schnittstellen Bezeichner. Verwenden Sie den **IBackgroundCopyFile2** -Schnittstellen Zeiger, um die [**ibackgroundcopyfile**](ibackgroundcopyfile.md) -Methode und die **IBackgroundCopyFile2** -Methode aufzurufen.

## <a name="members"></a>Member

Die **IBackgroundCopyFile2** -Schnittstelle erbt von [**ibackgroundcopyfile**](ibackgroundcopyfile.md). **IBackgroundCopyFile2** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IBackgroundCopyFile2** -Schnittstelle verfügt über diese Methoden.



| Methode                                                             | BESCHREIBUNG                                                                      |
|:-------------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [**Getfileranges**](ibackgroundcopyfile2-getfileranges-method.md) | Ruft das Array von Bereichen ab, die Sie aus der URL herunterladen möchten.<br/> |
| [**Servername**](ibackgroundcopyfile2-setremotename-method.md) | Ändert den Remote Namen in eine neue URL.<br/>                                 |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1709, \[ nur Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, Version 1709, \[ nur Desktop-Apps\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Deliveryoptimization. idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyFile2 ist als 83e81b93-0873-474d-8a8c-f 2018b1a939c definiert.<br/>             |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ibackgroundcopyfile**](ibackgroundcopyfile.md)
</dt> </dl>

 

 





