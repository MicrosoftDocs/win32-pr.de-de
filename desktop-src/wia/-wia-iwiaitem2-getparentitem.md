---
description: Ruft das übergeordnete Element in der-Struktur ab, das ein Windows-Abbild Erfassungs-Hardware Gerät (WIA) 2,0 darstellt.
ms.assetid: c6fdaf1d-9875-4852-893c-813894d89f6c
title: 'IWiaItem2:: getparameentitem-Methode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.GetParentItem
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 055625b98807103c3b79109216f6081d00564b15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343668"
---
# <a name="iwiaitem2getparentitem-method"></a>IWiaItem2:: getparameentitem-Methode

Ruft das übergeordnete Element in der-Struktur ab, das ein Windows-Abbild Erfassungs-Hardware Gerät (WIA) 2,0 darstellt.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetParentItem(
  [out] IWiaItem2 **ppIWiaItem2
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppIWiaItem2* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***

Empfängt die Adresse eines Zeigers auf die [**IWiaItem2**](-wia-iwiaitem2.md) -Schnittstelle des übergeordneten Elements des Elements in der Struktur von Item-Objekten. Wenn diese Methode für den Stamm der Struktur aufgerufen wird, ist die zurückgegebene Adresse **null**.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Wenn ein beliebiges [**IWiaItem2**](-wia-iwiaitem2.md) -Objekt in der Objektstruktur eines WIA 2,0-Hardware Geräts vorhanden ist, ruft die Anwendung einen Zeiger auf das übergeordnete Element ab, indem diese Funktion aufgerufen wird.

Anwendungen müssen die [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) -Methode für die Schnittstellen Zeiger aufrufen, die Sie über den *ppIWiaItem2* -Parameter empfangen, wenn diese Zeiger nicht **null** sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
