---
description: Legt diesen Zeiger auf eine Element Bezeichner-Liste (PIDL) als ungültigen Teil des shellordners.
title: 'Ishellfoldersearchable:: invalidatesearch-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderSearchable.InvalidateSearch
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 6985a299-8547-4db4-99f9-d46dafe4789b
ms.openlocfilehash: 36c1de0a606fdfddbe8eb74b5cc6c20cdda8e983
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214870"
---
# <a name="ishellfoldersearchableinvalidatesearch-method"></a>Ishellfoldersearchable:: invalidatesearch-Methode

Legt diesen Zeiger auf eine Element Bezeichner-Liste (PIDL) als ungültigen Teil des shellordners.

## <a name="syntax"></a>Syntax


```C++
HRESULT InvalidateSearch(
  [in] LPCITEMIDLIST pidlSearch,
  [in] DWORD         *pdwFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pidlsearch* \[ in\]
</dt> <dd>

Typ: **lpcitemittellist**

Ein Zeiger auf die [**itemittellist**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) -Struktur für den Suchordner.

</dd> <dt>

*pdwflags* \[ in\]
</dt> <dd>

Typ: **DWORD \** _

Zurzeit sind keine Flags definiert. Legen Sie auf _ * NULL * * fest.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Wenn ein Suchordner ungültig wird, kann er die Bereinigung aller verwendeten Ressourcen ausführen. Die **ishellfoldersearchable:: invalidatesearch** -Methode kann bewirken, dass eine asynchrone Suche abgebrochen wird, und führt dazu, dass das [**ishellfoldersearchablecallback**](ishellfoldersearchablecallback.md) -Schnittstellen Objekt die endgültige Version enthält.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                             |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 




