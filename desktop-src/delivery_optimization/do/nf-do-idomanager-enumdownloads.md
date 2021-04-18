---
title: 'Idomanager:: enumdownloads-Methode'
description: Ruft einen Schnittstellen Zeiger auf ein Enumeratorobjekt ab, das verwendet wird, um vorhandene Downloads aufzulisten.
keywords:
- 'Idomanager:: enumdownloads-Methode'
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
ms.openlocfilehash: a1e7fed2955fdc1b5ac0c11cfebc34aa95517603
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2019
ms.locfileid: "106338037"
---
# <a name="idomanagerenumdownloads-method"></a>Idomanager:: enumdownloads-Methode

Ruft einen Schnittstellen Zeiger auf ein Enumeratorobjekt ab, das verwendet wird, um vorhandene Downloads aufzulisten.

## <a name="syntax"></a>Syntax

```cpp
HRESULT EnumDownloads(
  DO_DOWNLOAD_ENUM_CATEGORY *category, 
  IEnumUnknown **ppEnum
);
```

## <a name="parameters"></a>Parameter

`category`

Optional. Der Eigenschaftsname, der als Kategorie für die Aufzählung verwendet werden soll. Durch die Übergabe `nullptr` werden alle vorhandenen Downloads abgerufen. Die folgenden Eigenschaften werden als Kategorie unterstützt.

- **DODownloadProperty_Id**
- **DODownloadProperty_Uri**
- **DODownloadProperty_ContentId**
- **DODownloadProperty_DisplayName**
- **DODownloadProperty_LocalPath**

`ppEnum`

Die Adresse eines Schnittstellen Zeigers auf **IEnumUnknown**, der zum Aufzählen vorhandener Downloads verwendet wird. Der Inhalt des Enumerators hängt vom Wert der *Kategorie* ab. Die Downloads, die in der Enumerationsschnittstelle enthalten sind, sind diejenigen, die zuvor vom gleichen Aufrufer dieser Funktion erstellt wurden. 

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, wird **S_OK** zurückgegeben. Andernfalls wird ein [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) - [Fehlercode](/windows/desktop/com/com-error-codes-10)zurückgegeben.

## <a name="requirements"></a>Anforderungen

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Unterstützte Mindestversion (Client)** | Nur Windows 10, Version 1809, \[ Win32-Anwendungen\] |
| **Unterstützte Mindestversion (Server)** | Nur Windows Server, Version 1809, \[ Win32-Anwendungen\] |
| **Header** | Do. h |
