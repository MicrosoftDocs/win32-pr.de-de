---
description: Ruft Typinformationen eines Elements ab.
ms.assetid: 9670f184-e8ba-4596-af6d-2967320dfd95
title: 'IWiaItem2:: GetItemType-Methode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.GetItemType
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 3bf177ddcc117cdfe21a1b9322a0e457cf899c0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751784"
---
# <a name="iwiaitem2getitemtype-method"></a>IWiaItem2:: GetItemType-Methode

Ruft Typinformationen eines Elements ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetItemType(
  [out] LONG *pItemType
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pitemtype* \[ vorgenommen\]
</dt> <dd>

Type: **Long \** _

Empfängt einen Zeiger auf ein _ *Long**, das eine Kombination von typfflags enthält. Siehe [**WIA-Elementtyp-Flags**](-wia-wia-item-type-flags.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Jedes [**IWiaItem2**](-wia-iwiaitem2.md) -Objekt in der hierarchischen Struktur von Objekten, das einem Windows-Abbild Erfassungs-Hardware Gerät (WIA) 2,0 zugeordnet ist, verfügt über einen bestimmten Datentyp. Element Objekte stellen Ordner und Dateien dar. Ordner enthalten Datei Objekte. Datei Objekte enthalten Daten, die vom Gerät abgerufen werden, z. b. Bilder und Sounds. Diese Methode ermöglicht Anwendungen, den Typ jedes Elements in einer hierarchischen Struktur von Element Objekten in einem Gerät zu identifizieren.

Ein Element kann über mehr als einen Typ verfügen. Beispielsweise verfügt ein Element, das eine Audiodatei darstellt, über die Typattribute [**wiaitemtypeaudiowiaitemtypefile**](-wia-wia-item-type-flags.md) \| .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 




