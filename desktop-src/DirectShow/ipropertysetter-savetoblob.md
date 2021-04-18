---
description: Die savetoblob-Methode speichert die Eigenschaften Daten in einem Persistenzformat.
ms.assetid: 48201192-abda-484e-bdb3-442aca52b2bf
title: 'Ipropertysetter:: savedeblob-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.SaveToBlob
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 97e248ebf741b45e73c82b17eee4181b1f19ac35
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365499"
---
# <a name="ipropertysettersavetoblob-method"></a>Ipropertysetter:: savedeblob-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `SaveToBlob` Methode speichert die Eigenschaften Daten in einem Persistenzformat.

## <a name="syntax"></a>Syntax


```C++
HRESULT SaveToBlob(
  [out] LONG *pcSize,
  [out] BYTE **ppb
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pcsize* \[ vorgenommen\]
</dt> <dd>

Empfängt die Größe der Daten in Bytes.

</dd> <dt>

*ppb* \[ vorgenommen\]
</dt> <dd>

Empfängt einen Zeiger auf ein Bytearray, das die Daten empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Die-Methode ordnet Speicher für das Bytearray zu. Der Aufrufer muss ihn mithilfe der **CoTaskMemFree** -Funktion freigeben.

Alle Eigenschaftsnamen und-Werte werden auf eine Länge von 40 Zeichen gekürzt. Aus diesem Grund ist XML das bevorzugte Persistenzformat. Siehe [**IXml2Dex-Schnittstelle**](ixml2dex.md).

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

[**Ipropertysetter-Schnittstelle**](ipropertysetter.md)
</dt> <dt>

[Fehler-und Erfolgs Codes](error-and-success-codes.md)
</dt> </dl>

 

 




