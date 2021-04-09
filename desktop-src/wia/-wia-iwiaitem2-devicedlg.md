---
description: Zeigt dem Benutzer ein Dialogfeld an, in dem die Bild Erfassung vorbereitet werden soll.
ms.assetid: 2d7246ec-fb90-4538-b717-b9e3813c1696
title: IWiaItem2::D evicedlg-Methode (WIA. h)
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
ms.openlocfilehash: 3337e74a621b6431b5bbfa429692717def447c82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129429"
---
# <a name="iwiaitem2devicedlg-method"></a>IWiaItem2::D evicedlg-Methode

Zeigt dem Benutzer ein Dialogfeld an, in dem die Bild Erfassung vorbereitet werden soll.

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

*lFlags* \[ in\]
</dt> <dd>

Type: **Long**

Gibt einen Satz von Flags an, die den Vorgang des Dialog Felds steuern. Der Wert kann entweder 0 (null) sein, um das Standardverhalten darzustellen, oder eines der WIA- \_ Geräte \_ Dialogfelder, die in [**wiaflag**](-wia-wiaflag.md)beschrieben werden.

</dd> <dt>

*hwndParent* \[ in\]
</dt> <dd>

Typ: **HWND**

Ein Handle für das übergeordnete Fenster.

</dd> <dt>

*bstrinfoldername* \[ in\]
</dt> <dd>

Typ: **BSTR**

Gibt den Namen des Ordners an, in den die Dateien übertragen werden sollen.

</dd> <dt>

*bstrauch filename* \[ in\]
</dt> <dd>

Typ: **BSTR**

Gibt den Namen der Vorlagen Datei an.

</dd> <dt>

*plnumfiles* \[ in\]
</dt> <dd>

Type: **Long \** _

Ein Zeiger auf die Anzahl der Elemente im _ppbstrFilePaths *-Array.

</dd> <dt>

*ppbstraufilepfade* \[ in, out\]
</dt> <dd>

Typ: **BSTR \* \***

Die Adresse eines Zeigers auf ein Array von Pfaden für die gescannten Dateien. Initialisieren Sie den Zeiger, um auf ein Array der Größe 0 (null) vor IWiaItem2 zu zeigen **::D evicedlg** aufgerufen wird.

</dd> <dt>

*ppIWiaItem2* \[ in, out\]
</dt> <dd>

Typ: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***

Die Adresse eines Arrays von Zeigern auf [**IWiaItem2**](-wia-iwiaitem2.md) -Schnittstellen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Diese Methode zeigt dem Benutzer ein Dialogfeld an, das von einer Anwendung verwendet wird, um alle für die Image Erfassung erforderlichen Informationen zu sammeln. Sie wird auch verwendet, um Bild Scan Eigenschaften anzugeben, z. b. Helligkeit und Kontrast.

Nachdem diese Methode zurückgegeben wurde, kann die Anwendung die [**iwiatransfer**](-wia-iwiatransfer.md) -Schnittstelle verwenden, um das Image abzurufen.

Anwendungen müssen die [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) -Methode für jedes Element im Array von Schnittstellen Zeigern aufrufen, die über den *ppIWiaItem2* -Parameter empfangen werden. Anwendungen müssen das Array auch mit " [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree)" freigeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
