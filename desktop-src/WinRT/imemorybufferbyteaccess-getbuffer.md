---
description: Ruft ein imemorybuffer-Element als Bytearray ab.
ms.assetid: E9C2AF2D-ADBE-4D76-A549-2DBCB9818B09
title: 'Imemorybufferbyteaccess:: GetBuffer-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMemoryBufferByteAccess.GetBuffer
api_type:
- COM
api_location: ''
ms.openlocfilehash: f31d1506822f21977e2d60492248c2d70a51829c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353074"
---
# <a name="imemorybufferbyteaccessgetbuffer-method"></a>Imemorybufferbyteaccess:: GetBuffer-Methode

Ruft ein [**imemorybuffer**](/uwp/api/Windows.Foundation.IMemoryBuffer?view=winrt-19041) -Element als Bytearray ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetBuffer(
  [out] BYTE   **value,
  [out] UINT32 *capacity
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Wert* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf ein Bytearray, das die Puffer Daten enthält.

</dd> <dt>

*Kapazität* \[ vorgenommen\]
</dt> <dd>

Die Anzahl der Bytes im zurückgegebenen Array.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Wenn [**memorybuffer:: Close**](/uwp/api/Windows.Foundation.MemoryBuffer?view=winrt-19041) aufgerufen wird, sollte der Code, der diesen Puffer verwendet, den *Wert* Zeiger auf NULL festlegen.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Imemorybufferbyteaccess**](/previous-versions//mt297505(v=vs.85))
</dt> </dl>

 

 
