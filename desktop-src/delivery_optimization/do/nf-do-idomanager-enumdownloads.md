---
title: IDOManager::EnumDownloads-Methode
description: Ruft einen Schnittstellenzeiger auf ein Enumeratorobjekt ab, das zum Aufzählen vorhandener Downloads verwendet wird.
keywords:
- IDOManager::EnumDownloads-Methode
topic_type:
- apiref
api_name:
- IDOManager.EnumDownloads
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 5442196b95e654755b4f84fe85375afb8f5b9372ddae453ca4ddffb567882fda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118543827"
---
# <a name="idomanagerenumdownloads-method"></a>IDOManager::EnumDownloads-Methode

Ruft einen Schnittstellenzeiger auf ein Enumeratorobjekt ab, das zum Aufzählen vorhandener Downloads verwendet wird.

## <a name="syntax"></a>Syntax

```cpp
HRESULT EnumDownloads(
  DO_DOWNLOAD_ENUM_CATEGORY *category, 
  IEnumUnknown **ppEnum
);
```

## <a name="parameters"></a>Parameter

`category`

Optional. Der Eigenschaftsname, der als Kategorie zum Aufzählen verwendet werden soll. Durch `nullptr` die Übergabe werden alle vorhandenen Downloads abgerufen. Die folgenden Eigenschaften werden als Kategorie unterstützt.

- **DODownloadProperty_Id**
- **DODownloadProperty_Uri**
- **DODownloadProperty_ContentId**
- **DODownloadProperty_DisplayName**
- **DODownloadProperty_LocalPath**

`ppEnum`

Die Adresse eines Schnittstellenzeigers auf **IEnumUnknown,** der zum Aufzählen vorhandener Downloads verwendet wird. Der Inhalt des Enumerators hängt vom Wert der Kategorie *ab.* Die in der Enumerationsschnittstelle enthaltenen Downloads sind diejenigen, die zuvor vom gleichen Aufrufer dieser Funktion erstellt wurden. 

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, gibt **sie** S_OK. Andernfalls wird ein [**HRESULT-Fehlercode**](/windows/desktop/com/structure-of-com-error-codes) [zurückgegeben.](/windows/desktop/com/com-error-codes-10)

## <a name="requirements"></a>Anforderungen

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Unterstützte Mindestversion (Client)** | \[Windows 10, Version 1809 Nur Win32-Anwendungen\] |
| **Unterstützte Mindestversion (Server)** | Windows Server, version 1809 Win32 applications only (Nur \[ Win32-Anwendungen der Version 1809)\] |
| **Header** | Do.h |
