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
# <a name="dataformats"></a>DataFormats

Gibt die von einer Anwendung unterstützten Standard-und Hauptdaten Formate an.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      DataFormats
         DefaultFile = file/format
         GetSet
            n = formats
```

## <a name="remarks"></a>Bemerkungen

Der *Datei-/Formatwert* gibt die Standard Hauptdatei oder das Standard Objekt Format für Objekte dieser Klasse an.

Der *Formatwert* gibt eine Liste von Formaten für Standard Implementierungen von [**EnumFormatEtc**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-enumformatetc)an, wobei *n* ein NULL basierter ganzzahliger Index ist. Beispiel: *n*  =  *Format*, *Aspekt*, *Mittel*, *Flag*, wobei *Format* ein Zwischenablage Format ist, *Aspekt* ein oder mehrere Member von [**DVASPECT**](/windows/win32/api/wtypes/ne-wtypes-dvaspect), *Medium* ein oder mehrere Member von [**TYMED**](/windows/win32/api/objidl/ne-objidl-tymed)und *Flag* ein oder mehrere Member von [**datadir**](/windows/win32/api/objidl/ne-objidl-datadir)ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IDataObject:: EnumFormatEtc**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-enumformatetc)
</dt> <dt>

[**IDataObject:: GetData**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-getdata)
</dt> <dt>

[**IDataObject:: SetData**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-setdata)
</dt> </dl>

 

 




