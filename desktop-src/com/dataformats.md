---
title: Dataformats
description: Gibt die von einer Anwendung unterstützten Standard- und Hauptdatenformate an.
ms.assetid: 0c9387f9-d7e0-40e7-8d86-96a79a844161
keywords:
- DataFormats-Registrierungsschlüssel COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfb8b2cc2ad4d11137fa41f419db2184f1a2b47fb850176227401e3d2b1aec04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118310598"
---
# <a name="dataformats"></a>Dataformats

Gibt die von einer Anwendung unterstützten Standard- und Hauptdatenformate an.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      DataFormats
         DefaultFile = file/format
         GetSet
            n = formats
```

## <a name="remarks"></a>Hinweise

Der *Datei-/Formatwert* gibt das Standardmäßige Hauptdatei- oder Objektformat für Objekte dieser Klasse an.

Der *formats-Wert* gibt eine Liste von Formaten für Standardimplementierungen von [**EnumFormatEtc**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-enumformatetc)an, wobei *n* ein nullbasierter ganzzahliger Index ist. Beispiel: *n*  =  *format*, *aspect*, *medium*, *flag*, wobei *format* ein Zwischenablageformat ist, *aspect* ein oder mehrere Member von [**DVASPECT,**](/windows/win32/api/wtypes/ne-wtypes-dvaspect) *medium* ein oder mehrere Member von [**TYMED**](/windows/win32/api/objidl/ne-objidl-tymed)und *flag* ein oder mehrere Member von [**DATADIR**](/windows/win32/api/objidl/ne-objidl-datadir)ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IDataObject::EnumFormatEtc**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-enumformatetc)
</dt> <dt>

[**IDataObject::GetData**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-getdata)
</dt> <dt>

[**IDataObject::SetData**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-setdata)
</dt> </dl>

 

 




