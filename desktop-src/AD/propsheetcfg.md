---
title: PROPSHEETCFG-Struktur
description: Wird verwendet, um Konfigurationsdaten für Eigenschaftenblätter zu enthalten.
ms.assetid: d3bde744-9d85-4506-894f-f8be3463721f
ms.tgt_platform: multiple
keywords:
- PROPSHEETCFG-Struktur In Active Directory
- PPROPSHEETCFG-Strukturzeiger Active Directory
topic_type:
- apiref
api_name:
- PROPSHEETCFG
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 971296e1e269e977919f142d1efe24426b9c83f19ac26da2e2362ab48da0aa9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025438"
---
# <a name="propsheetcfg-structure"></a>PROPSHEETCFG-Struktur

Die **PROPSHEETCFG-Struktur** wird verwendet, um Konfigurationsdaten für Eigenschaftenblätter zu enthalten. Diese Struktur ist im [**CFSTR \_ DS \_ PROPSHEETCONFIG-Zwischenablageformat**](cfstr-ds-propsheetconfig.md) enthalten.

> [!Note]  
> Diese Struktur ist nicht in einer veröffentlichten Headerdatei definiert. Um diese Struktur zu verwenden, müssen Sie sie selbst im genauen formatierten Format definieren.

 

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

**lNotifyHandle**
</dt> <dd>

Enthält das Benachrichtigungshand handle. Dies ist identisch mit dem Handle, das für den *handle-Parameter* in der [**IExtendPropertySheet2::CreatePropertyPages-Methode übergeben**](/previous-versions/windows/desktop/legacy/aa814847(v=vs.85)) wird.

</dd> <dt>

**hwndParentSheet**
</dt> <dd>

Enthält das Fensterhand handle des übergeordneten Eigenschaftenblatts.

</dd> <dt>

**hwndHidden**
</dt> <dd>

Enthält das Handle des ausgeblendeten Fensters.

</dd> <dt>

**wParamSheetClose**
</dt> <dd>

Enthält einen anwendungsdefinierten 32-Bit-Wert. Dieser Wert wird in der *wParam-Datei* der [**WM \_ DSA \_ SHEET CLOSE \_ \_ NOTIFY-Meldung**](wm-dsa-sheet-close-notify.md) an die Anwendung übergeben.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CFSTR \_ DS \_ PROPSHEETCONFIG**](cfstr-ds-propsheetconfig.md)
</dt> <dt>

[**WM \_ DSA \_ SHEET \_ CLOSE \_ NOTIFY**](wm-dsa-sheet-close-notify.md)
</dt> </dl>

 

