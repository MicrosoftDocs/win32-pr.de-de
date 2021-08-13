---
title: DO_DOWNLOAD_ENUM_CATEGORY-Struktur
description: Wird von **IDOManager::EnumDownloads verwendet,** um die Downloadsenumeration nach dem Wert der jeweiligen Eigenschaft zu filtern.
keywords:
- DO_DOWNLOAD_ENUM_CATEGORY-Struktur
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
ms.openlocfilehash: 32bdc7ca9a84bfe87ff453d34c4ecff57a8dabf5f67b21cc0d54ba079efd1578
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118543758"
---
# <a name="do_download_enum_category-structure"></a>DO_DOWNLOAD_ENUM_CATEGORY-Struktur

Die **DO_DOWNLOAD_ENUM_CATEGORY** wird von **IDOManager::EnumDownloads** verwendet, um die Downloadsenumeration nach dem Wert der jeweiligen Eigenschaft zu filtern.

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

Der Eigenschaftsname, der für die Downloadenumeration verwendet werden soll. Diese Eigenschaften werden zu Enumerationszwecken unterstützt.
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
| **Unterstützte Mindestversion (Client)** | \[Windows 10, Version 1809 Nur Win32-Anwendungen\] |
| **Unterstützte Mindestversion (Server)** | Windows Server, version 1809 Win32 applications only (Nur \[ Win32-Anwendungen der Version 1809)\] |
| **Header** | Do.h |
