---
description: Erstellen Sie ein neues untergeordnetes Element. Fügt der IWiaItem2-Struktur eines Geräts IWiaItem2-Objekte hinzu.
ms.assetid: 525ee788-3ff4-4def-ae71-4a405c04c6a3
title: 'IWiaItem2:: kreatechilditem-Methode (WIA. h)'
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
ms.openlocfilehash: 0002a6110894491a8d6efabb5a142b7c81adc820
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349869"
---
# <a name="iwiaitem2createchilditem-method"></a>IWiaItem2:: kreatechilditem-Methode

Erstellen Sie ein neues untergeordnetes Element. Fügt der **IWiaItem2** -Struktur eines Geräts [**IWiaItem2**](-wia-iwiaitem2.md) -Objekte hinzu.

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

*litemflags* \[ in\]
</dt> <dd>

Type: **Long**

Gibt den WIA-2,0-Elementtyp an. Siehe [**WIA-Elementtyp-Flags**](-wia-wia-item-type-flags.md).

</dd> <dt>

*lkreationflags* \[ in\]
</dt> <dd>

Type: **Long**

Gibt an, wie das neue Element erstellt wird.

<dt>

<span id="0"></span>

<span id="0"></span>**0** (0)


</dt> <dd>

Legen Sie die Standardwerte für die Eigenschaften des untergeordneten Elements fest.

</dd> <dt>

<span id="COPY_PARENT_PROPERTY_VALUES"></span><span id="copy_parent_property_values"></span>

<span id="COPY_PARENT_PROPERTY_VALUES"></span><span id="copy_parent_property_values"></span>**Kopieren \_ Übergeordnete \_ Eigenschafts \_ Werte** (0x40000000)


</dt> <dd>

Kopieren Sie die Werte aller Lese-/Schreibeigenschaften von der übergeordneten.

</dd> </dl> </dd> <dt>

*bstritemname* \[ in\]
</dt> <dd>

Typ: **BSTR**

Gibt den Elementnamen an. Dieser Name wird an das Ende des Namens des übergeordneten Elements angehängt, um den vollständigen Elementnamen zu generieren.

</dd> <dt>

*ppIWiaItem2* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***

Empfängt die Adresse eines Zeigers auf die [**IWiaItem2**](-wia-iwiaitem2.md) -Schnittstelle, mit der die **IWiaItem2:: featechilditem** -Methode festgelegt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Einige WIA 2,0-Hardware Geräte ermöglichen es Anwendungen, neue Elemente in der [**IWiaItem2**](-wia-iwiaitem2.md) -Struktur zu erstellen, die das Gerät darstellt. Anwendungen müssen die Geräte testen, um festzustellen, ob Sie diese Funktion unterstützen. Verwenden Sie die ienumwia \_ dev \_ Caps-Oberfläche, um die Funktionen des aktuellen Geräts aufzulisten.

Wenn das Gerät das Erstellen neuer Elemente in der [**IWiaItem2**](-wia-iwiaitem2.md) -Struktur zulässt, wird durch Aufrufen von **IWiaItem2:: auflistungschilditem** ein neues **IWiaItem2** -Objekt erstellt, das dem aktuellen Knoten untergeordnet ist. Es übergibt einen Zeiger auf den neuen Knoten über den *ppIWiaItem2* -Parameter an die Anwendung. Anwendungen müssen die [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) -Methode für die Schnittstellen Zeiger aufrufen, die Sie über den *ppIWiaItem2* -Parameter empfangen.

Wenn *lkreationflags* den Wert von über \_ geordneten \_ Eigenschafts \_ Werten kopieren und *litemflags* 0 (null) ist, gibt die Funktion E \_ invalidArg zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
