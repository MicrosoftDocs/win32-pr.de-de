---
description: Zeigt dem Benutzer ein Dialogfeld an, um sich auf die Imageerfassung vorzubereiten.
ms.assetid: 2d7246ec-fb90-4538-b717-b9e3813c1696
title: IWiaItem2::D eviceDlg-Methode (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.DeviceDlg
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: c9eaab17f0a76bfc5c6ac919a9abef92ca7288539c9705ca30c02b1dd0a8d1ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118035221"
---
# <a name="iwiaitem2devicedlg-method"></a>IWiaItem2::D eviceDlg-Methode

Zeigt dem Benutzer ein Dialogfeld an, um sich auf die Imageerfassung vorzubereiten.

## <a name="syntax"></a>Syntax


```C++
HRESULT DeviceDlg(
  [in]      LONG      lFlags,
  [in]      HWND      hwndParent,
  [in]      BSTR      bstrFolderName,
  [in]      BSTR      bstrFilename,
  [in]      LONG      *plNumFiles,
  [in, out] BSTR      **ppbstrFilePaths,
  [in, out] IWiaItem2 **ppIWiaItem2
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lFlags* \[ In\]
</dt> <dd>

Typ: **LONG**

Gibt einen Satz von Flags an, die den Vorgang des Dialogfelds steuern. Der Wert kann entweder 0 sein, um das Standardverhalten darzustellen, oder eines der \_ \_ in [**WiaFlag**](-wia-wiaflag.md)beschriebenen WIA DEVICE DIALOG-Flags.

</dd> <dt>

*hwndParent* \[ In\]
</dt> <dd>

Typ: **HWND**

Ein Handle für das übergeordnete Fenster.

</dd> <dt>

*bstrFolderName* \[ In\]
</dt> <dd>

Typ: **BSTR**

Gibt den Ordnernamen an, in den die Dateien übertragen werden sollen.

</dd> <dt>

*bstrFilename* \[ In\]
</dt> <dd>

Typ: **BSTR**

Gibt den Namen der Vorlagendatei an.

</dd> <dt>

*plNumFiles* \[ In\]
</dt> <dd>

Typ: **\* LONG**

Ein Zeiger auf die Anzahl der Elemente im *ppbstrFilePaths-Array.*

</dd> <dt>

*ppbstrFilePaths* \[ in, out\]
</dt> <dd>

Typ: **BSTR \* \***

Die Adresse eines Zeigers auf ein Array von Pfaden für die gescannten Dateien. Initialisieren Sie den Zeiger so, dass er auf ein Array der Größe 0 (null) zeigt, bevor **IWiaItem2::D eviceDlg** aufgerufen wird.

</dd> <dt>

*ppIWiaItem2* \[ in, out\]
</dt> <dd>

Typ: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***

Die Adresse eines Arrays von Zeigern auf [**IWiaItem2-Schnittstellen.**](-wia-iwiaitem2.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Diese Methode zeigt dem Benutzer ein Dialogfeld an, in dem eine Anwendung alle für die Imageerfassung erforderlichen Informationen erfasst. Es wird auch verwendet, um Bildscaneigenschaften wie Helligkeit und Kontrast anzugeben.

Nachdem diese Methode zurückgegeben wurde, kann die Anwendung die [**IWiaTransfer-Schnittstelle**](-wia-iwiatransfer.md) verwenden, um das Bild zu erhalten.

Anwendungen müssen die [IUnknown::Release-Methode](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) für jedes Element im Array von Schnittstellenzeigern aufrufen, die sie über den *ppIWiaItem2-Parameter* empfangen. Anwendungen müssen das Array auch mit [coTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree)freigeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 
