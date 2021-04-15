---
title: IBackgroundCopyFile2 getfileranges-Methode (deliveryoptimization. h)
description: Ruft die Bereiche ab, die Sie aus der Remote Datei herunterladen möchten.
ms.assetid: 19B7B4FC-371F-482B-B997-C240B5483F4D
keywords:
- Getfileranges-Methode
- Getfileranges-Methode, IBackgroundCopyFile2-Schnittstelle
- IBackgroundCopyFile2 Interface, getfileranges-Methode
topic_type:
- apiref
api_name:
- IBackgroundCopyFile2.GetFileRanges
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 37352176ca460587343bed0a154ee992c12c2fff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391839"
---
# <a name="ibackgroundcopyfile2getfileranges-method"></a>IBackgroundCopyFile2:: getfileranges-Methode

Ruft die Bereiche ab, die Sie aus der Remote Datei herunterladen möchten.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetFileRanges(
  [in, out] DWORD         *RangeCount,
  [out]     BG_FILE_RANGE **Ranges
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Rangecount* \[ in, out\]
</dt> <dd>

Anzahl der Elemente in *Bereichen*.

</dd> <dt>

*Bereiche* \[ vorgenommen\]
</dt> <dd>

Array von [**BG_FILE_RANGE**](bg-file-range.md) Strukturen, die die Bereiche angeben, die heruntergeladen werden sollen. Wenn Sie den Vorgang abgeschlossen haben *, können Sie* die Funktion " [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) " aufrufen

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt sowohl die folgenden Rückgabewerte als auch andere zurück.



| Rückgabecode                                                                              | Beschreibung                                                                                                                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl> | Erfolg<br/>                                                                                                                            |
| <dl> <dt>**S_FALSE**</dt> </dl>  | Es wurden keine Bereiche angegeben, oder es handelt sich um einen Upload-oder Upload-Reply-Auftrag. *Rangecount* ist auf 0 (null) und *Bereiche* auf **null** festgelegt.<br/> |



 

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

[**BG_FILE_RANGE**](bg-file-range.md)
</dt> <dt>

[**IBackgroundCopyFile2**](ibackgroundcopyfile2.md)
</dt> </dl>

 

