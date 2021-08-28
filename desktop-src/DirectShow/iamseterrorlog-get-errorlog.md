---
description: Die get \_ ErrorLog-Methode ruft das aktuelle Fehlerprotokoll für dieses Objekt ab.
ms.assetid: 580b8a06-6bf2-49ef-a5fb-5e6df2f09793
title: IAMSetErrorLog::get_ErrorLog-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMSetErrorLog.get_ErrorLog
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 1ca9104ea1ea526719401d8974de51d356acb91b3c6539992fbcbe42c8a36d39
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102730"
---
# <a name="iamseterrorlogget_errorlog-method"></a>IAMSetErrorLog::get \_ ErrorLog-Methode

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

 

Die `get_ErrorLog` -Methode ruft das aktuelle Fehlerprotokoll für dieses Objekt ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_ErrorLog(
  [out, retval] IAMErrorLog **pVal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pVal* \[ out, retval\]
</dt> <dd>

Empfängt einen Zeiger auf die [**IAMErrorLog-Schnittstelle**](iamerrorlog.md) des Fehlerprotokolls. Wenn die Zeitachse kein Fehlerprotokoll enthält, wird der Wert auf **NULL festgelegt.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Wenn der in *pVal zurückgegebene* Wert nicht **NULL ist,** verfügt die [**IAMErrorLog-Schnittstelle**](iamerrorlog.md) über eine ausstehende Verweisanzahl. Stellen Sie sicher, dass Sie die -Schnittstelle wieder frei geben, wenn Sie sie nicht mehr verwenden.

> [!Note]  
> Die Headerdatei Qedit.h ist nicht mit Direct3D-Headern nach Version 7 kompatibel.

 

> [!Note]  
> Um Qedit.h zu erhalten, laden Sie das Microsoft Windows SDK-Update für Windows Vista und [.NET Framework 3.0 herunter.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IAMSetErrorLog-Schnittstelle**](iamseterrorlog.md)
</dt> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> </dl>

 

 




