---
title: DO_DOWNLOAD_ENUM_CATEGORY Struktur
description: 'Wird von **idomanager:: enumdownloads** verwendet, um die Downloads-Enumeration nach dem Wert der bestimmten Eigenschaft zu filtern.'
keywords:
- DO_DOWNLOAD_ENUM_CATEGORY Struktur
topic_type:
- apiref
api_name:
- DO_DOWNLOAD_ENUM_CATEGORY
api_location:
- do.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: a78c94cd9d8854453517976300e12a031f65b8cb
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2019
ms.locfileid: "106342105"
---
# <a name="do_download_enum_category-structure"></a>DO_DOWNLOAD_ENUM_CATEGORY Struktur

Die **DO_DOWNLOAD_ENUM_CATEGORY** Struktur wird von **idomanager:: enumdownloads** verwendet, um die Downloads-Enumeration nach dem Wert der bestimmten Eigenschaft zu filtern.

## <a name="syntax"></a>Syntax
```cpp
typedef struct _DO_DOWNLOAD_ENUM_CATEGORY
{
  DODownloadProperty Property;
  LPCWSTR Value;
} DO_DOWNLOAD_ENUM_CATEGORY;
```

## <a name="members"></a>Member

`Property`

Der Eigenschaftsname, der für die Download-Enumeration verwendet werden soll. Diese Eigenschaften werden für Enumerationszwecke unterstützt.
- **DODownloadProperty_Id**
- **DODownloadProperty_Uri**
- **DODownloadProperty_ContentId**
- **DODownloadProperty_DisplayName**
- **DODownloadProperty_LocalPath**

`Value`

Der Wert der Eigenschaft.

## <a name="requirements"></a>Anforderungen

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Unterstützte Mindestversion (Client)** | Nur Windows 10, Version 1809, \[ Win32-Anwendungen\] |
| **Unterstützte Mindestversion (Server)** | Nur Windows Server, Version 1809, \[ Win32-Anwendungen\] |
| **Header** | Do. h |
