---
title: oleautomation-Attribut
description: Mittel l oleautomation-Attribut und Kompatibilität mit Automation.
ms.assetid: 4a1c9a02-d637-4595-87b3-5fe903149357
keywords:
- oleautomation-Attribut-Mittel l
topic_type:
- apiref
api_name:
- oleautomation
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b827aba4cb0871f7130e658299c6d8836557a156
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038971"
---
# <a name="oleautomation-attribute"></a>oleautomation-Attribut

Das **oleautomation** -Attribut gibt an, dass eine Schnittstelle mit Automation kompatibel ist.

``` syntax
[ 
    oleautomation, 
    uuid(string-uuid)
    [ , interface-attribute-list] 
] 
interface interface-name : base-interface
{
    ...
}
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Zeichenfolge-UUID* 
</dt> <dd>

Gibt eine UUID-Zeichenfolge an, die vom Hilfsprogramm uuidgen generiert wird.

</dd> <dt>

*Interface-Attribute-List* 
</dt> <dd>

Gibt andere Attribute an, die auf die gesamte Schnittstelle angewendet werden.

</dd> <dt>

*Schnittstellen Name* 
</dt> <dd>

Gibt den Namen der Schnittstelle an.

</dd> <dt>

*Basisschnittstelle* 
</dt> <dd>

Gibt den Namen einer Automatisierungsschnittstelle an, von der diese abgeleitete Schnittstelle Member-Funktionen, Statuscodes und Schnittstellen Attribute erbt. Alle Automatisierungs Schnittstellen werden von [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) oder [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)abgeleitet.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Parameter und Rückgabe Typen, die für die Member einer **\[ oleautomation \]** -Schnittstelle angegeben werden, müssen Automatisierungs kompatibel sein, wie in der folgenden Tabelle aufgeführt.



| type                                            | BESCHREIBUNG                                                                                                                                                                                                   |
|-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **boolean**                                     | Ein Datenelement, das den Wert Variant \_ true oder Variant \_ false aufweisen kann. Die Größe entspricht Variant \_ bool.                                                                                                     |
| **unsigned char**                               | 8-Bit-Datenelement ohne Vorzeichen.                                                                                                                                                                                     |
| **double**                                      | 64-Bit-IEEE-Gleit Komma Zahl.                                                                                                                                                                            |
| **float**                                       | 32-Bit-IEEE-Gleit Komma Zahl.                                                                                                                                                                            |
| **int**                                         | Ganze Zahl mit Vorzeichen, deren Größe System abhängig ist. Auf 32-Bit-Plattformen behandelt die Mittel l [**int**](int.md) als eine 32-Bit-Ganzzahl mit Vorzeichen.                                                                               |
| **long**                                        | Ganze 32-Bit-Zahl mit Vorzeichen:                                                                                                                                                                                        |
| **short**                                       | 16-Bit-Ganzzahl mit Vorzeichen.                                                                                                                                                                                        |
| **BSTR**                                        | Zeichenfolge mit Längen Präfix, wie im Automation-Thema [BSTR](/previous-versions/windows/desktop/automat/bstr)beschrieben.                                                                                                    |
| **CURRENCY**                                    | 8-Byte-Gleit Komma Zahl mit fester Größe.                                                                                                                                                                          |
| **DATE**                                        | 64-Bit, Gleit Komma Zahl von Tagen seit dem 30. Dezember 1899.                                                                                                                                     |
| **SCODE**                                       | Für 16-Bit-Systeme – integrierter Fehlertyp, der dem VT- \_ Fehler entspricht.                                                                                                                                         |
| **Typedef** -Aufzählung - *Myerum*                      | Ganze Zahl mit Vorzeichen, deren Größe System abhängig ist.                                                                                                                                                               |
| **IDispatch-Schnittstelle \***                      | Zeiger auf die [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle (VT \_ Dispatch).                                                                                                                |
| **Schnittstelle IUnknown \***                       | Zeiger auf eine Schnittstelle, die nicht von [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) (VT \_ unknown) abgeleitet ist. (Eine beliebige OLE-Schnittstelle kann durch die [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle dargestellt werden.) |
| **dispinterface** " *Typname \** "                | Zeiger auf eine Schnittstelle, die von [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) (VT \_ Dispatch) abgeleitet ist.                                                                                                    |
| **Co-Klasse** " *Typname \** "                      | Zeiger auf einen Co-Klassennamen (VT \_ unknown).                                                                                                                                                                      |
| **\[ oleautomation- \] Schnittstelle**  *Typname \** | Zeiger auf eine Schnittstelle, die von [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)abgeleitet ist.                                                                                                                                      |
| **SAFEARRAY**(*Typname*)                       | *Typname* ist einer der oben genannten Typen. Array dieser Typen.                                                                                                                                                   |
| **TypeName \***                                 | *Typname* ist einer der oben genannten Typen. Zeiger auf einen Typ.                                                                                                                                                      |
| **Dezimal**                                     | 96-Bit-Ganzzahl ohne Vorzeichen, die durch eine Variablen Potenz von 10 skaliert wurde. Ein Decimal-Datentyp, der eine Größe und eine Skala für eine Zahl (wie in Koordinaten) bereitstellt.                                                       |



 

Ein Parameter ist mit Automation kompatibel, wenn der Typ ein Automatisierungs kompatibler Typ, ein Zeiger auf einen Automatisierungs kompatiblen Typ oder ein SAFEARRAY eines Automatisierungs kompatiblen Typs ist.

Ein Rückgabetyp ist mit Automation kompatibel, wenn der Typ ein HRESULT, SCODE oder [**void**](void.md)ist. Allerdings erfordert die Mittelwert Schnittstelle, dass Schnittstellen Methoden entweder HRESULT oder SCODE zurückgeben. Die Rückgabe von **void** generiert einen Compilerfehler.

Ein Member ist mit Automation kompatibel, wenn der Rückgabetyp und alle zugehörigen Parameter Automatisierungs kompatibel sind.

Eine Schnittstelle ist mit Automation kompatibel, wenn Sie von [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) oder [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)abgeleitet ist, das **\[ oleautomation \]** -Attribut aufweist und alle zugehörigen VTBL-Einträge Automatisierungs kompatibel sind. Bei 32-Bit-Plattformen muss die Aufruf Konvention für alle Methoden in der Schnittstelle stdcall lauten. Für 16-Bit-Systeme müssen alle Methoden über die Cdecl-Aufruf Konvention verfügen.

Jede [**dispinterface**](dispinterface.md) ist implizit Automatisierungs kompatibel. Daher sollten Sie das **\[ oleautomation \]** -Attribut nicht für **dispinterface** verwenden.

Das **\[ oleautomation \]** -Attribut ist nicht verfügbar, wenn Sie mit dem [**/OSF**](-osf.md) -Schalter für den Mittelwert Compiler kompilieren.

### <a name="flags"></a>Flags

TYPEFLAG \_ foleautomation

## <a name="examples"></a>Beispiele

``` syntax
library Hello
{
    importlib("stdole32.tlb");
    [
        uuid(12345678-1234-1234-1234-123456789ABC),
        helpstring("Application object for the Hello application."),
        oleautomation,
        dual
    ]
    interface IHello : IDispatch
    {
        // Interface definition statements.
    }

    // Other library definition statements.
}
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Schnittstellen Definitionsdatei (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[Erstellen einer Typbibliothek mit "Mittel l"](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[Beispiel für eine ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Syntax der ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**UUID**](uuid.md)
</dt> </dl>

 

 