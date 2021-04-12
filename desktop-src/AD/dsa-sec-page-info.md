---
title: DSA_SEC_PAGE_INFO Struktur
description: Wird mit dem Blatt "WM \_ adsprop \_ Sheet \_ Create" und "WM- \_ DSA" \_ \_ Erstellen \_ von Benachrichtigungs Meldungen zum Definieren eines sekundären Eigenschaften Blatts in einem Active Directory MMC-Snap-in verwendet.
ms.assetid: 422d84dc-6b5e-43bf-ac4f-3b99cb59f9df
ms.tgt_platform: multiple
keywords:
- DSA_SEC_PAGE_INFO Struktur Active Directory
- PDSA_SEC_PAGE_INFO Struktur Zeiger Active Directory
topic_type:
- apiref
api_name:
- DSA_SEC_PAGE_INFO
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e4c8602a958c50c72942d89657a812d24f64571d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956732"
---
# <a name="dsa_sec_page_info-structure"></a>DSA \_ sec- \_ Seite \_ Info-Struktur

Die **Informationen Struktur der DSA \_ sec- \_ Seite \_** wird mit dem Blatt " [**WM \_ adsprop \_ Sheet \_ Create**](wm-adsprop-sheet-create.md) " und " [**WM-DSA" Erstellen von \_ \_ \_ \_ Benachrichtigungs**](wm-dsa-sheet-create-notify.md) Meldungen zum Definieren eines sekundären Eigenschaften Blatts in einem Active Directory MMC-Snap-in verwendet.

> [!Note]  
> Diese Struktur ist nicht in einer veröffentlichten Header Datei definiert. Um diese Struktur zu verwenden, definieren Sie Sie im exakten Format.

 

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

**hwndparametrisheet**
</dt> <dd>

Enthält das Fenster Handle des übergeordneten Elements des sekundären Eigenschaften Blatts.

</dd> <dt>

**offsettitle**
</dt> <dd>

Enthält den Offset in Bytes vom Anfang der **DSA- \_ \_ Seiten \_ Info** Struktur zu einer auf NULL endenden Unicode-Zeichenfolge, die den Titel des sekundären Eigenschaften Blatts enthält.

</dd> <dt>

**dsobjectnames**
</dt> <dd>

Enthält eine [**dsobjectnames**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) -Struktur, die das sekundäre Eigenschaften Blatt definiert. Es kann immer nur ein sekundäres Eigenschaften Blatt erstellt werden. Daher kann die **dsobjectnames** -Struktur nur eine [**dsobject**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) -Struktur enthalten.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**WM- \_ adsprop- \_ Blatt \_ Erstellen**](wm-adsprop-sheet-create.md)
</dt> <dt>

[**WM \_ - \_ Blatt "DSA \_ Erstellen \_ "**](wm-dsa-sheet-create-notify.md)
</dt> <dt>

[**Dsobjectnames**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames)
</dt> <dt>

[**Dsobject**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject)
</dt> </dl>

 

 





