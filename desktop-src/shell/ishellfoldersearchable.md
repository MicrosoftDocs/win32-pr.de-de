---
description: Macht Methoden verfügbar, mit denen eine Shellerweiterung einen durchsuchbaren Namespace bereitstellen kann.
title: Ishellfoldersearchable-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderSearchable
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 359def5c-d7ad-46bd-bdda-30a7b3eea56c
ms.openlocfilehash: 1f42b3af012361bfd24c93e03c38e6954eb5326e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977944"
---
# <a name="ishellfoldersearchable-interface"></a>Ishellfoldersearchable-Schnittstelle

Macht Methoden verfügbar, mit denen eine Shellerweiterung einen durchsuchbaren Namespace bereitstellen kann.

## <a name="members"></a>Member

Die **ishellfoldersearchable** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Ishellfoldersearchable** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ishellfoldersearchable** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                | BESCHREIBUNG                                                               |
|:----------------------------------------------------------------------|:--------------------------------------------------------------------------|
| [**Cancelasyncsearch**](ishellfoldersearchable-cancelasyncsearch.md) | Startet das Abbrechen einer ausstehenden asynchronen Suche.<br/> |
| [**FindString**](ishellfoldersearchable-findstring.md)               | Startet eine Suche nach einer angegebenen Such Zeichenfolge.<br/>                 |
| [**Invalidatesearch**](ishellfoldersearchable-invalidatesearch.md)   | Macht diese PIDL zu einem ungültigen Teil des shellordners.<br/>        |



 

## <a name="remarks"></a>Bemerkungen

Diese Schnittstelle ist in keinen öffentlichen Header Dateien definiert. Wenn Sie diese Schnittstelle implementieren möchten, können Sie den folgenden C/C++-Code verwenden, um die zugehörigen Methoden zu deklarieren.


```
#undef  INTERFACE
#define INTERFACE IShellFolderSearchable
DECLARE_INTERFACE_IID_(IShellFolderSearchable, IUnknown, "4E1AE66C-204B-11d2-8DB3-0000F87A556C")
{
    // **_ IUnknown methods _*_
    STDMETHOD(QueryInterface) (THIS_ REFIID riid, __out void _*ppv) PURE;
    STDMETHOD_(ULONG,AddRef)  (THIS) PURE;
    STDMETHOD_(ULONG,Release) (THIS) PURE;

    // **_ IShellFolderSearchable methods _*_

    // FindString -
    //  The returned Shell folder's enumerator will have any
    //   search hits for the given search string.
    //  punkOnAsyncSearch will be QI'd for IShellFolderSearchableCallback
    STDMETHOD(FindString)(THIS_ LPCWSTR pwszTarget, __inout_opt DWORD _pdwFlags,
                          __in_opt IUnknown *punkOnAsyncSearch, __out LPITEMIDLIST *ppidlOut)   PURE;
    // CancelAsyncSearch -
    //   Begins the process of canceling any pending
    //    asynchronous search from this pidl.
    //    When the search is actually canceled, RunEnd will be called
    //   Returns: S_OK => cancelling, S_FALSE => not running
    STDMETHOD(CancelAsyncSearch) (THIS_ LPCITEMIDLIST pidlSearch, __inout_opt DWORD *pdwFlags) PURE;

    // InvalidateSearch -
    //   Makes this pidl no longer a valid portion of the Shell folder
    //    Also does some cleanup of any databases used in the search and
    //    will cause the eventual release of the callback
    //   May cause async search to be canceled
    STDMETHOD(InvalidateSearch)  (THIS_ LPCITEMIDLIST pidlSearch, __inout_opt DWORD *pdwFlags) PURE;
};
```



## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                             |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 
