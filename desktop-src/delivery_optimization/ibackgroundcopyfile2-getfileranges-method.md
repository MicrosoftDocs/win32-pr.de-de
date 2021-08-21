---
title: IBackgroundCopyFile2 GetFileRanges-Methode (Deliveryoptimization.h)
description: Ruft die Bereiche ab, die Sie aus der Remotedatei herunterladen möchten.
ms.assetid: 19B7B4FC-371F-482B-B997-C240B5483F4D
keywords:
- GetFileRanges-Methode
- GetFileRanges-Methode, IBackgroundCopyFile2-Schnittstelle
- IBackgroundCopyFile2-Schnittstelle, GetFileRanges-Methode
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
ms.openlocfilehash: 156bb2eb1e136593bfec4310599200f2d2800e271defa0e4a3259a4a67acb648
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047078"
---
# <a name="ibackgroundcopyfile2getfileranges-method"></a>IBackgroundCopyFile2::GetFileRanges-Methode

Ruft die Bereiche ab, die Sie aus der Remotedatei herunterladen möchten.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetFileRanges(
  [in, out] DWORD         *RangeCount,
  [out]     BG_FILE_RANGE **Ranges
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*RangeCount* \[ in, out\]
</dt> <dd>

Anzahl der Elemente in *Ranges*.

</dd> <dt>

*Bereiche* \[ out\]
</dt> <dd>

Array von [**BG_FILE_RANGE**](bg-file-range.md) Strukturen, die die herunterzuladende Bereiche angeben. Rufen Sie anschließend die [**CoTaskMemFree-Funktion**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) auf, um Ranges frei zu *machen.*

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt die folgenden Rückgabewerte sowie andere zurück.



| Rückgabecode                                                                              | Beschreibung                                                                                                                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S_OK</dt> </dl> | Erfolg<br/>                                                                                                                            |
| <dl> <dt>**S_FALSE**</dt> </dl>  | Es wurden keine Bereiche angegeben, oder der Auftrag ist ein Upload- oder Upload-Reply-Auftrag. *RangeCount* ist auf 0 (null) und *Ranges* auf **NULL** festgelegt.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, nur Desktop-Apps der Version 1709 \[\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, nur Desktop-Apps der Version 1709 \[\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyFile2 ist als 83e81b93-0873-474d-8a8c-f2018b1a939c definiert.<br/>             |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**BG_FILE_RANGE**](bg-file-range.md)
</dt> <dt>

[**IBackgroundCopyFile2**](ibackgroundcopyfile2.md)
</dt> </dl>

 

