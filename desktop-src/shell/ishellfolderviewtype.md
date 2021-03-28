---
description: Macht Methoden verfügbar, mit denen ein Shellordner verschiedene Ansichten für seinen Inhalt unterstützt (verschiedene hierarchische Layouts der Daten).
title: Ishellfolderviewtype-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderViewType
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 9b597f6b-ef27-4fa1-ad00-e131dbd979e7
ms.openlocfilehash: 1440b6d14950ad70d2c76168b28bb1077b19b5a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042242"
---
# <a name="ishellfolderviewtype-interface"></a>Ishellfolderviewtype-Schnittstelle

Macht Methoden verfügbar, mit denen ein Shellordner verschiedene Ansichten für seinen Inhalt unterstützt (verschiedene hierarchische Layouts der Daten).

## <a name="members"></a>Member

Die **ishellfolderviewtype** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Ishellfolderviewtype** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ishellfolderviewtype** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                      | BESCHREIBUNG                                                                                                                                                          |
|:----------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Enumsichten**](ishellfolderviewtype-enumviews.md)                         | Ruft einen Enumerator ab, der eine PIDL für jede erweiterte Ansicht zurückgibt.<br/>                                                                                |
| [**Getdefaultviewname**](ishellfolderviewtype-getdefaultviewname.md)       | Ruft den Namen der Standardansicht ab. Rufen Sie [**IShellFolder:: GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) auf, um die Namen der anderen Sichten abzurufen.<br/> |
| [**Getviewtypeproperties**](ishellfolderviewtype-getviewtypeproperties.md) | Ruft die Eigenschaften der Ansicht ab.<br/>                                                                                                                          |
| [**Translateviewpidl**](ishellfolderviewtype-translateviewpidl.md)         | Rekonstruiert eine PIDL aus einer hierarchischen Darstellung des shellordners in eine andere Darstellung.<br/>                                             |



 

## <a name="remarks"></a>Bemerkungen

Dieser Enumerator gibt pidls zurück, bei denen es sich um besondere ausgeblendete Ordner auf der obersten Ebene des shellordners handelt, die ansonsten nicht aufgelistet werden. Die Standardansicht ist die Standardansicht, die im Shellordner normal angezeigt wird.

Diese Schnittstelle ist in keiner öffentlichen Header Datei definiert. Wenn Sie diese Schnittstelle implementieren möchten, können Sie den folgenden C/C++-Code verwenden, um die zugehörigen Methoden zu deklarieren.


```
#undef  INTERFACE
#define INTERFACE   IShellFolderViewType
DECLARE_INTERFACE_IID_(IShellFolderViewType, IUnknown, "49422C1E-1C03-11d2-8DAB-0000F87A556C")
{
    // **_ IUnknown methods _*_
    STDMETHOD(QueryInterface) (THIS_ REFIID riid, __out void _*ppv) PURE;
    STDMETHOD_(ULONG,AddRef)  (THIS) PURE;
    STDMETHOD_(ULONG,Release) (THIS) PURE;

    // **_ IShellFolderViewType Methods _*_

    // EnumViews:
    //   Returns an enumerator which will give out one pidl for every extended view.
    STDMETHOD(EnumViews)(THIS_ ULONG grfFlags, __out IEnumIDList _*ppenum) PURE;

    // GetDefaultViewName:
    //   Returns the name of the default view.  The names of the other views
    //   can be retrieved by calling GetDisplayNameOf.
    STDMETHOD(GetDefaultViewName)(THIS_ DWORD  uFlags, __out LPWSTR *ppwszName) PURE;
    STDMETHOD(GetViewTypeProperties)(THIS_ PCUITEMID_CHILD pidl, __out DWORD *pdwFlags)  PURE;

    // TranslateViewPidl:
    //   Attempts to take a pidl represented in one hierarchical representation of
    //   the Shell folder, and find it in a different representation.
    //   pidl should be relative to the root folder.
    //   Remember to ILFree ppidlOut
    STDMETHOD(TranslateViewPidl)(THIS_ PCUIDLIST_RELATIVE pidl, PCUIDLIST_RELATIVE pidlView,
              __out PIDLIST_RELATIVE *ppidlOut) PURE;
};

#define SFVTFLAG_NOTIFY_CREATE  0x00000001
#define SFVTFLAG_NOTIFY_RESORT  0x00000002
```



## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                             |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 
