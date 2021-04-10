---
title: IBackgroundCopyFile5-Schnittstelle (deliveryoptimization. h)
description: Verwenden Sie diese Schnittstelle, um allgemeine Eigenschaften von Dateiübertragungen zur Übermittlungs Optimierung (Do) zu erhalten oder festzulegen.
ms.assetid: 2D729717-62D2-4C69-92FE-F4289EC48DF1
keywords:
- IBackgroundCopyFile5-Schnittstelle
- IBackgroundCopyFile5-Schnittstelle, beschrieben
topic_type:
- apiref
api_name:
- IBackgroundCopyFile5
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2f23fdb99ba24b4faeca7a65930bf83d4634a979
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103506"
---
# <a name="ibackgroundcopyfile5-interface"></a>IBackgroundCopyFile5-Schnittstelle

Verwenden Sie diese Schnittstelle, um allgemeine Eigenschaften von Dateiübertragungen zur Übermittlungs Optimierung (Do) zu erhalten oder festzulegen.

Um einen **IBackgroundCopyFile5** -Schnittstellen Zeiger abzurufen, verwenden Sie die **ibackgroundcopyfile:: QueryInterface** -Methode mithilfe __uuidof (IBackgroundCopyFile5) für den Schnittstellen Bezeichner.

## <a name="members"></a>Member

Die **IBackgroundCopyFile5** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **IBackgroundCopyFile5** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IBackgroundCopyFile5** -Schnittstelle verfügt über diese Methoden.



| Methode                                                  | BESCHREIBUNG                                                         |
|:--------------------------------------------------------|:--------------------------------------------------------------------|
| [**GetProperty**](ibackgroundcopyfile5-getproperty.md) | Ruft den Wert einer generischen backgroundcopyfile-Eigenschaft ab.<br/> |
| [**SetProperty**](ibackgroundcopyfile5-setproperty.md) | Legt den Wert einer generischen backgroundcopyfile-Eigenschaft fest.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1709, \[ nur Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, Version 1709, \[ nur Desktop-Apps\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Deliveryoptimization. idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyFile5 ist als "85c1657f-DAFC-40e8-8834-df18ea25717e" definiert.<br/>             |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ibackgroundcopyfile**](ibackgroundcopyfile.md)
</dt> <dt>

[**IBackgroundCopyFile2**](ibackgroundcopyfile2.md)
</dt> </dl>

 

