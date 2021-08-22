---
title: DSA_SEC_PAGE_INFO-Struktur
description: Wird mit den NACHRICHTEN WM ADSPROP SHEET CREATE und WM DSA SHEET CREATE NOTIFY verwendet, um ein sekundäres Eigenschaftenblatt in einem \_ \_ Active Directory \_ \_ \_ \_ \_ MMC-Snap-In zu definieren.
ms.assetid: 422d84dc-6b5e-43bf-ac4f-3b99cb59f9df
ms.tgt_platform: multiple
keywords:
- DSA_SEC_PAGE_INFO Active Directory-Struktur
- PDSA_SEC_PAGE_INFO Strukturzeiger Active Directory
topic_type:
- apiref
api_name:
- DSA_SEC_PAGE_INFO
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 26fa3dcfb983de8e1052b319bac7c3a594e256b594847c32b553353e6caee17d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118695648"
---
# <a name="dsa_sec_page_info-structure"></a>DSA \_ SEC \_ PAGE \_ INFO-Struktur

Die **DSA \_ SEC PAGE \_ \_ INFO-Struktur** wird mit [**den NACHRICHTEN WM \_ ADSPROP SHEET \_ \_ CREATE**](wm-adsprop-sheet-create.md) und [**WM \_ DSA SHEET CREATE \_ \_ \_ NOTIFY**](wm-dsa-sheet-create-notify.md) verwendet, um ein sekundäres Eigenschaftenblatt in einem Active Directory MMC-Snap-In zu definieren.

> [!Note]  
> Diese Struktur ist nicht in einer veröffentlichten Headerdatei definiert. Um diese Struktur zu verwenden, definieren Sie sie im genauen angezeigten Format.

 

## <a name="syntax"></a>Syntax


```C++
typedef struct _DSA_SEC_PAGE_INFO {
  HWND          hwndParentSheet;
  DWORD         offsetTitle;
  DSOBJECTNAMES dsObjectNames;
} DSA_SEC_PAGE_INFO, *PDSA_SEC_PAGE_INFO;
```



## <a name="members"></a>Member

<dl> <dt>

**hwndParentSheet**
</dt> <dd>

Enthält das Fensterhand handle des übergeordneten Elements des sekundären Eigenschaftenblatts.

</dd> <dt>

**offsetTitle**
</dt> <dd>

Enthält den Offset in Bytes vom Anfang der **SEC \_ PAGE \_ \_ INFO-Struktur** des DSA zu einer mit NULL beendeten Unicode-Zeichenfolge, die den Titel des sekundären Eigenschaftenblatts enthält.

</dd> <dt>

**dsObjectNames**
</dt> <dd>

Enthält eine [**DSOBJECTNAMES-Struktur,**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) die das sekundäre Eigenschaftenblatt definiert. Es kann immer nur ein sekundäres Eigenschaftenblatt erstellt werden, sodass die **DSOBJECTNAMES-Struktur** nur eine [**DSOBJECT-Struktur enthalten**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) kann.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**WM \_ ADSPROP \_ SHEET \_ CREATE**](wm-adsprop-sheet-create.md)
</dt> <dt>

[**WM \_ DSA \_ SHEET \_ CREATE \_ NOTIFY**](wm-dsa-sheet-create-notify.md)
</dt> <dt>

[**DSOBJECTNAMES**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames)
</dt> <dt>

[**DSOBJECT**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject)
</dt> </dl>

 

 





