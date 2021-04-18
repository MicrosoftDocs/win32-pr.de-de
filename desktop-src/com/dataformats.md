---
title: DataFormats
description: Gibt die von einer Anwendung unterstützten Standard-und Hauptdaten Formate an.
ms.assetid: 0c9387f9-d7e0-40e7-8d86-96a79a844161
keywords:
- DataFormats-Registrierungsschlüssel com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf130461a8db67cfe7fc7c56b0115b27eef6dc6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340862"
---
# <a name="dataformats"></a><span data-ttu-id="548df-104">DataFormats</span><span class="sxs-lookup"><span data-stu-id="548df-104">DataFormats</span></span>

<span data-ttu-id="548df-105">Gibt die von einer Anwendung unterstützten Standard-und Hauptdaten Formate an.</span><span class="sxs-lookup"><span data-stu-id="548df-105">Specifies the default and main data formats supported by an application.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="548df-106">Registrierungseintrag</span><span class="sxs-lookup"><span data-stu-id="548df-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      DataFormats
         DefaultFile = file/format
         GetSet
            n = formats
```

## <a name="remarks"></a><span data-ttu-id="548df-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="548df-107">Remarks</span></span>

<span data-ttu-id="548df-108">Der *Datei-/Formatwert* gibt die Standard Hauptdatei oder das Standard Objekt Format für Objekte dieser Klasse an.</span><span class="sxs-lookup"><span data-stu-id="548df-108">The *file/format* value specifies the default main file or object format for objects of this class.</span></span>

<span data-ttu-id="548df-109">Der *Formatwert* gibt eine Liste von Formaten für Standard Implementierungen von [**EnumFormatEtc**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-enumformatetc)an, wobei *n* ein NULL basierter ganzzahliger Index ist.</span><span class="sxs-lookup"><span data-stu-id="548df-109">The *formats* value specifies a list of formats for default implementations of [**EnumFormatEtc**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-enumformatetc), where *n* is a zero-based integer index.</span></span> <span data-ttu-id="548df-110">Beispiel: *n*  =  *Format*, *Aspekt*, *Mittel*, *Flag*, wobei *Format* ein Zwischenablage Format ist, *Aspekt* ein oder mehrere Member von [**DVASPECT**](/windows/win32/api/wtypes/ne-wtypes-dvaspect), *Medium* ein oder mehrere Member von [**TYMED**](/windows/win32/api/objidl/ne-objidl-tymed)und *Flag* ein oder mehrere Member von [**datadir**](/windows/win32/api/objidl/ne-objidl-datadir)ist.</span><span class="sxs-lookup"><span data-stu-id="548df-110">For example, *n* = *format*, *aspect*, *medium*, *flag*, where *format* is a clipboard format, *aspect* is one or more members of [**DVASPECT**](/windows/win32/api/wtypes/ne-wtypes-dvaspect), *medium* is one or more members of [**TYMED**](/windows/win32/api/objidl/ne-objidl-tymed), and *flag* is one or more members of [**DATADIR**](/windows/win32/api/objidl/ne-objidl-datadir).</span></span>

## <a name="related-topics"></a><span data-ttu-id="548df-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="548df-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="548df-112">**IDataObject:: EnumFormatEtc**</span><span class="sxs-lookup"><span data-stu-id="548df-112">**IDataObject::EnumFormatEtc**</span></span>](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-enumformatetc)
</dt> <dt>

[<span data-ttu-id="548df-113">**IDataObject:: GetData**</span><span class="sxs-lookup"><span data-stu-id="548df-113">**IDataObject::GetData**</span></span>](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-getdata)
</dt> <dt>

[<span data-ttu-id="548df-114">**IDataObject:: SetData**</span><span class="sxs-lookup"><span data-stu-id="548df-114">**IDataObject::SetData**</span></span>](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-setdata)
</dt> </dl>

 

 




