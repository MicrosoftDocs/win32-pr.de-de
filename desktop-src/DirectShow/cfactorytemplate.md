---
description: Stellt eine Vorlage zum Erstellen von Klassen factorys zur
ms.assetid: 3dbe6402-15f8-4490-9fe2-bebaa4e79170
title: CFactoryTemplate-Klasse (Combase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CFactoryTemplate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1f9fbc76fe65e1f1136fb44d22db36500c4d8870f97befa8e36fa08a108ada71
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697620"
---
# <a name="cfactorytemplate-class"></a>CFactoryTemplate-Klasse

Stellt eine Vorlage zum Erstellen von Klassen factorys zur

In DirectShow werden Klassenfactorys mithilfe der **CFactoryTemplate-Klasse** spezialisiert, die auch als *Factoryvorlage bezeichnet wird.* Jede Klassen factory enthält einen Zeiger auf eine Factoryvorlage. Die Factoryvorlage enthält Informationen zu einem COM-Objekt, einschließlich des Klassenbezeichners (CLSID) des Objekts und eines Zeigers auf eine Funktion, die das Objekt erstellt.

Deklarieren Sie in Ihrer DLL ein globales Array von Factoryvorlagen mit dem Namen *g \_ Templates*. Schließen Sie eine Factoryvorlage für jedes Objekt in die DLL ein. Wenn die [**DllGetClassObject-Funktion**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject) eine neue Klassen factory erstellt, durchsucht sie das Array nach einer Vorlage mit einer übereinstimmenden CLSID. Wenn eine gefunden wird, wird eine Klassen factory erstellt, die einen Zeiger auf die übereinstimmende Vorlage enthält. Wenn der Client **IClassFactory::CreateInstance** aufruft, ruft die Klassenfactory die instanziierte Funktion auf, die in der Vorlage definiert ist.

Weitere Informationen finden Sie unter [Erstellen einer DirectShow-Filter-DLL.](how-to-create-a-dll.md)



| Öffentliche Membervariablen                                                   | Beschreibung                                                                |
|---------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [**m \_ Name**](cfactorytemplate-m-name.md)                                | Name des Filters.                                                        |
| [**m \_ ClsID**](cfactorytemplate-m-clsid.md)                              | Zeiger auf die CLSID des Objekts.                                        |
| [**m \_ lpfnNew**](cfactorytemplate-m-lpfnnew.md)                          | Zeiger auf eine Funktion, die eine Instanz des -Objekts erstellt.              |
| [**m \_ lpfnInit**](cfactorytemplate-m-lpfninit.md)                        | Zeiger auf eine Funktion, die vom DLL-Einstiegspunkt aufgerufen wird.           |
| [**m \_ pAMovieSetup-Filter \_**](cfactorytemplate-m-pamoviesetup-filter.md) | Zeiger auf eine [**AMOVIESETUP-FILTER-Struktur. \_**](amoviesetup-filter.md) |
| Öffentliche Methoden                                                            | Beschreibung                                                                |
| [**IsClassID**](cfactorytemplate-isclassid.md)                           | Bestimmt, ob eine CLSID dieser Klassenvorlage entspricht.                    |
| [**CreateInstance**](cfactorytemplate-createinstance.md)                 | Ruft die Objekterstellungsfunktion für die -Klasse auf.                          |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Combase.h (include Streams.h)</dt> </dl>                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib; </dt> <dt>Strmbasd.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Basisklassenreferenz](base-class-reference.md)
</dt> </dl>

 

