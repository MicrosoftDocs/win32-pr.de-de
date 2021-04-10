---
title: Propsheetcfg-Struktur
description: Wird verwendet, um Eigenschaften Blatt-Konfigurationsdaten zu enthalten.
ms.assetid: d3bde744-9d85-4506-894f-f8be3463721f
ms.tgt_platform: multiple
keywords:
- Propsheetcfg-Struktur Active Directory
- Ppropsheetcfg-Struktur Zeiger Active Directory
topic_type:
- apiref
api_name:
- PROPSHEETCFG
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 33f4a1186cc756435cc49ed7c81592385faaee60
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040644"
---
# <a name="propsheetcfg-structure"></a>Propsheetcfg-Struktur

Die **propsheetcfg** -Struktur wird verwendet, um Eigenschaften Blatt-Konfigurationsdaten zu enthalten. Diese Struktur ist im " [**cfstr \_ DS \_ propsheetconfig**](cfstr-ds-propsheetconfig.md) "-Zwischenablage Format enthalten.

> [!Note]  
> Diese Struktur ist nicht in einer veröffentlichten Header Datei definiert. Um diese Struktur verwenden zu können, müssen Sie Sie im exakten Format definieren.

 

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  LONG_PTR lNotifyHandle;
  HWND     hwndParentSheet;
  HWND     hwndHidden;
  WPARAM   wParamSheetClose;
} PROPSHEETCFG, *PPROPSHEETCFG;
```



## <a name="members"></a>Member

<dl> <dt>

**lnotifyhandle**
</dt> <dd>

Enthält das Benachrichtigungs handle. Dies ist identisch mit dem Handle, das für den *handle* -Parameter in der [**IExtendPropertySheet2:: deatepropertypages**](/previous-versions/windows/desktop/legacy/aa814847(v=vs.85)) -Methode übergeben wird.

</dd> <dt>

**hwndparametrisheet**
</dt> <dd>

Enthält das Fenster Handle des übergeordneten Eigenschaften Blatts.

</dd> <dt>

**hwndhidden**
</dt> <dd>

Enthält das Handle des ausgeblendeten Fensters.

</dd> <dt>

**wparamsheetclose**
</dt> <dd>

Enthält einen von der Anwendung definierten 32-Bit-Wert. Dieser Wert wird an die Anwendung in der *wParam* des [**WM-DSA- \_ Blatts \_ " \_ Close \_ Notify**](wm-dsa-sheet-close-notify.md) Message" zurückgegeben.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**cfstr \_ DS \_ propsheetconfig**](cfstr-ds-propsheetconfig.md)
</dt> <dt>

[**WM- \_ DSA- \_ Blatt " \_ Schließen \_ "**](wm-dsa-sheet-close-notify.md)
</dt> </dl>

 

