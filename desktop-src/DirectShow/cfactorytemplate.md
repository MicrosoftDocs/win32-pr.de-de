---
description: Bietet eine Vorlage zum Erstellen von Klassenfactorys.
ms.assetid: 3dbe6402-15f8-4490-9fe2-bebaa4e79170
title: Cfactorytemplate-Klasse (ComBase. h)
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
ms.openlocfilehash: be5ca9b8319eeddf777cbf0071c1930f21524369
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359639"
---
# <a name="cfactorytemplate-class"></a>Cfactorytemplate-Klasse

Bietet eine Vorlage zum Erstellen von Klassenfactorys.

In DirectShow werden **Klassenfactorys mithilfe der cfactorytemplate** -Klasse, die auch als Factoryvorlage bezeichnet wird, spezialisiert.  Jede Klassenfactory enthält einen Zeiger auf eine Factoryvorlage. Die Factoryvorlage enthält Informationen über ein COM-Objekt, einschließlich des Klassen Bezeichners (CLSID) des Objekts und eines Zeigers auf eine Funktion, die das Objekt erstellt.

Deklarieren Sie in der dll ein globales Array von fabricvorlagen mit dem Namen *g- \_ Vorlagen*. Fügen Sie für jedes Objekt in der DLL eine Factory-Vorlage ein. Wenn die [**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject) -Funktion eine neue Klassenfactory erstellt, durchsucht Sie das Array nach einer Vorlage mit einer entsprechenden CLSID. Wenn Sie einen gefunden hat, wird eine Klassenfactory erstellt, die einen Zeiger auf die entsprechende Vorlage enthält. Wenn der Client **IClassFactory:: kreateinstance** aufruft, ruft die Klassenfactory die in der Vorlage definierte instanzizierungsfunktion auf.

Weitere Informationen finden Sie unter [Erstellen einer DirectShow-Filter-DLL](how-to-create-a-dll.md).



| Öffentliche Element Variablen                                                   | BESCHREIBUNG                                                                |
|---------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [**m- \_ Name**](cfactorytemplate-m-name.md)                                | Name des Filters.                                                        |
| [**m \_ CLSID**](cfactorytemplate-m-clsid.md)                              | Zeiger auf die CLSID des Objekts.                                        |
| [**m \_ lpfnnew**](cfactorytemplate-m-lpfnnew.md)                          | Ein Zeiger auf eine Funktion, die eine Instanz des-Objekts erstellt.              |
| [**m \_ lpfninit**](cfactorytemplate-m-lpfninit.md)                        | Ein Zeiger auf eine Funktion, die vom DLL-Einstiegspunkt aufgerufen wird.           |
| [**m- \_ pamoviesetup- \_ Filter**](cfactorytemplate-m-pamoviesetup-filter.md) | Zeiger auf eine [**amoviesetup- \_ Filter**](amoviesetup-filter.md) Struktur. |
| Öffentliche Methoden                                                            | BESCHREIBUNG                                                                |
| [**Isclassid**](cfactorytemplate-isclassid.md)                           | Bestimmt, ob eine CLSID dieser Klassen Vorlage entspricht.                    |
| [**CreateInstance**](cfactorytemplate-createinstance.md)                 | Ruft die Objekt Erstellungs Funktion für die-Klasse auf.                          |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>ComBase. h (Include Streams. h)</dt> </dl>                                                    |
| Bibliothek<br/> | <dl> " <dt>Ermbase. lib;</dt> " " <dt>Straumbasd. lib</dt> " </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Basisklassen Referenz](base-class-reference.md)
</dt> </dl>

 

