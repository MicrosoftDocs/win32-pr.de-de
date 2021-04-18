---
title: Ibackgroundcopyfile-Schnittstelle (deliveryoptimization. h)
description: Ibackgroundcopyfile enthält Informationen zu einer Datei, die Teil eines Auftrags ist. Beispielsweise können Sie die ibackgroundcopyfile-Methoden verwenden, um die lokalen und Remote Namen der Datei abzurufen und Statusinformationen zu übertragen.
ms.assetid: 463ED61A-D7C5-4B44-97CF-FDAA138CE9E3
keywords:
- Ibackgroundcopyfile-Schnittstelle
- Ibackgroundcopyfile-Schnittstelle, beschrieben
topic_type:
- apiref
api_name:
- IBackgroundCopyFile
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3e4a54a66dee87770326d2456cb384e9d77f15e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337506"
---
# <a name="ibackgroundcopyfile-interface"></a>Ibackgroundcopyfile-Schnittstelle

**Ibackgroundcopyfile** enthält Informationen zu einer Datei, die Teil eines Auftrags ist. Beispielsweise können Sie die **ibackgroundcopyfile** -Methoden verwenden, um die lokalen und Remote Namen der Datei abzurufen und Statusinformationen zu übertragen.

Um einen **ibackgroundcopyfile** -Schnittstellen Zeiger abzurufen, müssen Sie die [**ibackgroundcopyerror:: GetFile**](ibackgroundcopyerror-getfile-method.md) -Methode oder die [**ienumbackgroundcopyfiles:: Next**](ienumbackgroundcopyfiles-next.md) -Methode aufrufen.

## <a name="members"></a>Member

Die **ibackgroundcopyfile** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Ibackgroundcopyfile** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ibackgroundcopyfile** -Schnittstelle verfügt über diese Methoden.



| Methode                                                            | BESCHREIBUNG                                             |
|:------------------------------------------------------------------|:--------------------------------------------------------|
| [**GetLocalName**](ibackgroundcopyfile-getlocalname-method.md)   | Ruft den lokalen Namen der Datei ab.<br/>        |
| [**GetProgress**](ibackgroundcopyfile-getprogress-method.md)     | Ruft den Fortschritt der Dateiübertragung ab.<br/> |
| [**Getremutename**](ibackgroundcopyfile-getremotename-method.md) | Ruft den Remote Namen der Datei ab.<br/>       |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1709, \[ nur Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, Version 1709, \[ nur Desktop-Apps\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Deliveryoptimization. idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyFile ist als 01b7bd23-B88-4a77-8490-5891d3e4653a definiert.<br/>              |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ibackgroundcopyerror**](ibackgroundcopyerror.md)
</dt> <dt>

[**IBackgroundCopyFile2**](ibackgroundcopyfile2.md)
</dt> <dt>

[**IBackgroundCopyJob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**Ienumbackgroundcopyfiles**](ienumbackgroundcopyfiles-.md)
</dt> </dl>

 

