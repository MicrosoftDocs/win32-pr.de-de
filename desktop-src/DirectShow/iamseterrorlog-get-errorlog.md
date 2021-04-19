---
description: Die get \_ ErrorLog-Methode ruft das aktuelle Fehlerprotokoll für dieses Objekt ab.
ms.assetid: 580b8a06-6bf2-49ef-a5fb-5e6df2f09793
title: 'Iamenterrorlog:: get_ErrorLog-Methode (qedit. h)'
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
ms.openlocfilehash: 508a73d6475698dca628de7e3bb96001fe13bcd0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369642"
---
# <a name="iamseterrorlogget_errorlog-method"></a>Iamseterrorlog:: get \_ ErrorLog-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `get_ErrorLog` Methode ruft das aktuelle Fehlerprotokoll für dieses-Objekt ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_ErrorLog(
  [out, retval] IAMErrorLog **pVal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PVal* \[ Out, retval\]
</dt> <dd>

Empfängt einen Zeiger auf die [**iamerrorlog**](iamerrorlog.md) -Schnittstelle des Fehler Protokolls. Wenn die Zeitachse kein Fehlerprotokoll enthält, wird der Wert auf **null** festgelegt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Wenn der in *PVal* zurückgegebene Wert nicht **null** ist, weist die [**iamerrorlog**](iamerrorlog.md) -Schnittstelle einen ausstehenden Verweis Zähler auf. Stellen Sie sicher, dass Sie die-Schnittstelle freigeben, wenn Sie Sie nicht mehr benötigen.

> [!Note]  
> Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.

 

> [!Note]  
> Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter. "Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>"Qedit. h"</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>"" "" ". Lib"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iameinterrorlog-Schnittstelle**](iamseterrorlog.md)
</dt> <dt>

[Fehler-und Erfolgs Codes](error-and-success-codes.md)
</dt> </dl>

 

 




