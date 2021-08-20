---
description: Erstellen Sie ein neues untergeordnetes Element. Fügt IWiaItem2-Objekte zur IWiaItem2-Struktur eines Geräts hinzu.
ms.assetid: 525ee788-3ff4-4def-ae71-4a405c04c6a3
title: IWiaItem2::CreateChildItem-Methode (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.CreateChildItem
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: e7d7215f528c36f6b4f5883be19d5d37c8b76d4d8ad9cacbcaa7a63397337c7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965569"
---
# <a name="iwiaitem2createchilditem-method"></a>IWiaItem2::CreateChildItem-Methode

Erstellen Sie ein neues untergeordnetes Element. Fügt [**IWiaItem2-Objekte**](-wia-iwiaitem2.md) zur **IWiaItem2-Struktur eines Geräts** hinzu.

## <a name="syntax"></a>Syntax


```C++
HRESULT CreateChildItem(
  [in]  LONG      lItemFlags,
  [in]  LONG      lCreationFlags,
  [in]  BSTR      bstrItemName,
  [out] IWiaItem2 **ppIWiaItem2
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lItemFlags* \[ In\]
</dt> <dd>

Typ: **LONG**

Gibt den WIA 2.0-Elementtyp an. Siehe [**WIA-Elementtypflags**](-wia-wia-item-type-flags.md).

</dd> <dt>

*lCreationFlags* \[ In\]
</dt> <dd>

Typ: **LONG**

Gibt an, wie das neue Element erstellt wird.

<dt>

<span id="0"></span>

<span id="0"></span>**0** (0)


</dt> <dd>

Legen Sie die Standardwerte für die Eigenschaften des untergeordneten -Werts fest.

</dd> <dt>

<span id="COPY_PARENT_PROPERTY_VALUES"></span><span id="copy_parent_property_values"></span>

<span id="COPY_PARENT_PROPERTY_VALUES"></span><span id="copy_parent_property_values"></span>**COPY \_ PARENT \_ PROPERTY \_ VALUES** (0x40000000)


</dt> <dd>

Kopieren Sie die Werte aller Lese-/Schreibeigenschaften aus dem übergeordneten Element.

</dd> </dl> </dd> <dt>

*bstrItemName* \[ In\]
</dt> <dd>

Typ: **BSTR**

Gibt den Elementnamen an. Dieser Name wird an das Ende des Namens des übergeordneten Elements angefügt, um den vollständigen Elementnamen zu generieren.

</dd> <dt>

*ppIWiaItem2* \[ out\]
</dt> <dd>

Typ: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***

Empfängt die Adresse eines Zeigers auf die [**IWiaItem2-Schnittstelle,**](-wia-iwiaitem2.md) die die **IWiaItem2::CreateChildItem-Methode legt.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Einige WIA 2.0-Hardwaregeräte ermöglichen Es Anwendungen, neue Elemente in der [**IWiaItem2-Struktur**](-wia-iwiaitem2.md) zu erstellen, die das Gerät darstellt. Anwendungen müssen die Geräte testen, um zu prüfen, ob sie diese Funktion unterstützen. Verwenden Sie die IEnumWIA DEV CAPS-Schnittstelle, um die Funktionen des aktuellen \_ \_ Geräts aufzählen.

Wenn das Gerät die Erstellung neuer Elemente in der [**IWiaItem2-Struktur**](-wia-iwiaitem2.md) zulässt, wird durch den Aufruf von **IWiaItem2::CreateChildItem** ein neues **IWiaItem2-Objekt** erstellt, das dem aktuellen Knoten untergeordnetes Objekt ist. Er übergibt einen Zeiger auf den neuen Knoten über den *ppIWiaItem2-Parameter* an die Anwendung. Anwendungen müssen die [IUnknown::Release-Methode für](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) die Schnittstellenzeigen aufrufen, die sie über den *ppIWiaItem2-Parameter* erhalten.

Wenn *lCreationFlags* COPY PARENT PROPERTY VALUES und \_ \_ \_ *lItemFlags* 0 (null) ist, gibt die Funktion E \_ INVALIDARG zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 
