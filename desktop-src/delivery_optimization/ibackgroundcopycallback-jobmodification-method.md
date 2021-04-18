---
title: Ibackgroundcopycallback jobänderungs-Methode (deliveryoptimization. h)
description: Die Übermittlungs Optimierung (Do) ruft Ihre Implementierung der jobmodifizierungsmethode auf, wenn der Auftrag geändert wurde.
ms.assetid: 4AC2575F-57FB-45E6-B29C-12DF615237F3
keywords:
- Jobänderungs-Methode
- Jobmodifikations Methode, ibackgroundcopycallback-Schnittstelle
- Ibackgroundcopycallback-Schnittstelle, jobmodifizierungs Methode
topic_type:
- apiref
api_name:
- IBackgroundCopyCallback.JobModification
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ceeb390fc8592c1e8e1d03efdb432056bd131a6e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337318"
---
# <a name="ibackgroundcopycallbackjobmodification-method"></a>Ibackgroundcopycallback:: jobänderungs-Methode

Die Übermittlungs Optimierung (Do) ruft Ihre Implementierung der [**jobmodifizierungsmethode**](https://www.bing.com/search?q=**JobModification**) auf, wenn der Auftrag geändert wurde. Der Dienst generiert dieses Ereignis, wenn Bytes übertragen werden, Dateien dem Auftrag hinzugefügt wurden, Eigenschaften geändert wurden oder sich der Status des Auftrags geändert hat.

## <a name="syntax"></a>Syntax


```C++
HRESULT JobModification(
  [in] IBackgroundCopyJob *pJob,
  [in] DWORD              dwReserved
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pjob* \[ in\]
</dt> <dd>

Enthält die Methoden zum Zugreifen auf Eigenschafts-, Status-und Zustandsinformationen des Auftrags. *Pjob* nicht freigeben; Gibt die-Schnittstelle frei, wenn die [**jobänderungs**](https://www.bing.com/search?q=**JobModification**) -Methode zurückgibt.

</dd> <dt>

*dwReserved* \[ in\]
</dt> <dd>

Für die zukünftige Verwendung reserviert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode sollte S_OK zurückgeben.

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

[**Ibackgroundcopycallback**](ibackgroundcopycallback.md)
</dt> <dt>

[**IBackgroundCopyJob**](ibackgroundcopyjob-.md)
</dt> </dl>

 

 





