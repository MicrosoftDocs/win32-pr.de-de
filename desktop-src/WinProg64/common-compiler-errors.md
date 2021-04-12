---
title: Häufige Compilerfehler
description: In diesem Abschnitt werden typische Compilerfehler veranschaulicht, die beim Migrieren einer vorhandenen Codebasis auftreten. Diese Beispiele stammen aus dem HAL-Code auf Systemebene, obwohl die Konzepte direkt auf Code auf Benutzerebene anwendbar sind.
ms.assetid: bbb6a57f-281a-4a6e-a4b6-15846d0cf21f
keywords:
- Compilerfehler 64-Bit-Windows-Programmierung
- Migration 64-Bit-Windows-Programmierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a84a5f5f58f2cab7555ce3401ed6fae0af240f4
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104316803"
---
# <a name="common-compiler-errors"></a>Häufige Compilerfehler

In diesem Abschnitt werden typische Compilerfehler veranschaulicht, die beim Migrieren einer vorhandenen Codebasis auftreten. Diese Beispiele stammen aus dem HAL-Code auf Systemebene, obwohl die Konzepte direkt auf Code auf Benutzerebene anwendbar sind.

## <a name="warning-c4311-example-1"></a>Warnung C4311 Beispiel 1

"Typumwandlung": Zeiger Verkürzung von "void \* \_ \_ ptr64" in "unsigned long"

<dl> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>Ordnung
</dt> <dd>

`pPciAddr->u.AsULONG = (ULONG) CIA_PCI_CONFIG_BASE_QVA;`

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Beschreibung
</dt> <dd>

**Ptrtoulong** ist abhängig von ihrer Verwendung eine Inline Funktion oder ein Makro. Ein Zeiger auf einen **ulong**-Wert wird abgeschnitten. Obwohl 32-Bit-Zeiger nicht betroffen sind, wird die obere Hälfte eines 64-Bit-Zeigers abgeschnitten.

Die CIA \_ PCI- \_ Konfigurations Basis- \_ \_ QVA ist als **pVoid** deklariert. Der **ulong** Cast funktioniert in der 32-Bit-Welt, führt jedoch zu einem Fehler in der 64-Bit-Welt. Die Lösung besteht darin, einen 64-Bit-Zeiger auf einen **ulong**-Wert zu erhalten, da das Ändern der Definition der Union, die ppciaddr->u. AsULong definiert ist, zu viel Code ändert.

Die Verwendung des Makros **ptrtoulong** zum Konvertieren der 64-Bit- **pVoid** in den benötigten **ulong** -Wert ist zulässig, da wir wissen über den spezifischen Wert der CIA- \_ PCI- \_ Konfigurations Basis- \_ \_ QVA verfügen. In diesem Fall enthält dieser Zeiger niemals Daten in den oberen 32 Bits.

</dd> <dt>

<span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Not
</dt> <dd>

`pPciAddr->u.AsULONG = PtrToUlong(CIA_PCI_CONFIG_BASE_QVA);`

</dd> </dl>

## <a name="warning-c4311-example-2"></a>Warnung C4311 Beispiel 2

"Typumwandlung": Zeiger Verkürzung von "struct \_ Error \_ Frame \* \_ \_ ptr64" in "unsigned long"

<dl> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>Ordnung
</dt> <dd>

`KeBugCheckEx( DATA_BUS_ERROR,0,0,0,(ULONG)PUncorrectableError );`

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Beschreibung
</dt> <dd>

Das Problem besteht darin, dass der letzte Parameter für diese Funktion ein Zeiger auf eine Datenstruktur ist. Da puncorrectableerror ein Zeiger ist, ändert sich die Größe mit dem Programmiermodell. Der Prototyp für **kebugcheckex** wurde geändert, sodass der letzte Parameter ein **ulong- \_ ptr** ist. Daher ist es erforderlich, den Funktionszeiger in ein **ulong- \_ ptr** umzuwandeln.

Sie können Fragen, warum **pVoid** nicht als letzter Parameter verwendet wurde. Je nach Kontext des Aufrufes ist der letzte Parameter möglicherweise etwas anderes als ein Zeiger oder möglicherweise ein Fehlercode.

</dd> <dt>

<span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Not
</dt> <dd>

`KeBugCheckEx( DATA_BUS_ERROR,0,0,0,(ULONG_PTR)PUncorrectableError );`

</dd> </dl>

## <a name="warning-c4244-example-1"></a>Warnung C4244 Beispiel 1

"=": Konvertierung von "struct \_ Configuration \_ Component \* \_ \_ ptr64" in "struct \_ Configuration \_ Component \* ", möglicher Datenverlust

<dl> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>Ordnung
</dt> <dd>

`Component = &CurrentEntry->ComponentEntry;`

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Beschreibung
</dt> <dd>

Die-Funktion deklariert die Variablen Komponente als pconfiguration- \_ Komponente. Später wird die Variable in der folgenden Zuweisung verwendet, die korrekt angezeigt wird:

`Component = &CurrentEntry->ComponentEntry;`

Der Typ "pconfiguration" \_ ist jedoch wie folgt definiert:

``` syntax
typedef struct __CONFIGURATION_COMPONENT {
...
...
} CONFIGURATION_COMPONENT, * POINTER_32 PCONFIGURATION_COMPONENT;
```

Die Typdefinition für die pconfiguration \_ -Komponente stellt einen 32-Bit-Zeiger sowohl in 32-Bit-als auch in 64-Bit-Modellen bereit, da Sie als **Zeiger \_ 32** deklariert ist. Der ursprüngliche Designer dieser Struktur wusste, dass er in einem 32-Bit-Kontext im BIOS verwendet und ausdrücklich für diese Verwendung definiert wurde. Dieser Code funktioniert problemlos in 32-Bit-Fenstern, da die Zeiger 32-Bit sind. In 64-Bit-Fenstern funktioniert es nicht, da sich der Code im 64-Bit-Kontext befindet.

</dd> <dt>

<span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Not
</dt> <dd>

Um dieses Problem zu umgehen, verwenden Sie \_ die Konfigurationskomponente \* anstelle der 32-Bit-pconfiguration- \_ Komponente. Es ist wichtig, dass Sie den Zweck des Codes eindeutig verstehen. Wenn dieser Code das 32-Bit-BIOS oder den System Raum berühren soll, funktioniert diese Korrektur nicht.

Der **Zeiger \_ 32** ist in "ntdef. h" und "Winnt. h" definiert.

``` syntax
#ifdef (__AXP64__)
#define POINTER_32 _ptr32
#else
#define POINTER_32
#endif
```

</dd> </dl>

## <a name="warning-c4242-example-2"></a>Warnung C4242 Beispiel 2

"=": Konvertierung von " \_ \_ Int64" in "unsigned long", möglicher Datenverlust

<dl> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>Ordnung
</dt> <dd>

``` syntax
ARC_STATUS HalpCopyNVRamBuffer (
IN PCHAR NvDestPtr,
IN PCHAR NvSrcPtr,
IN ULONG Length )
{

ULONG PageSelect1, ByteSelect1;

ByteSelect1 = (NvDestPtr - (PUCHAR)HalpCMOSRamBase) & CONFIG_RAM_BYTE_MASK;

ByteSelect1 = (NvDestPtr - (PUCHAR)HalpCMOSRamBase) & CONFIG_RAM_BYTE_MASK;
```

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Beschreibung
</dt> <dd>

Diese Warnung wird generiert, da die Berechnung 64-Bit-Werte verwendet, in diesem Fall Zeiger und das Ergebnis in einem 32-Bit- **ulong** platzieren.

</dd> <dt>

<span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Not
</dt> <dd>

Geben Sie das Ergebnis der Berechnung in ein **ulong** -Ergebnis ein, wie hier gezeigt:

`ByteSelect1 = (ULONG)(NvDestPtr - (PUCHAR)HalpCMOSRamBase) & CONFIG_RAM_BYTE_MASK;`

Typecasting das Ergebnis ermöglicht dem Compiler, dass Sie sich über das Ergebnis sicher sind. Das heißt, dass Sie die Berechnung verstehen und sicher sind, dass Sie in einen 32-Bit- **ulong** passt.

Wenn das Ergebnis möglicherweise nicht in einen 32-Bit- **ulong** passt, ändern Sie den Basistyp der Variablen, die das Ergebnis enthalten soll.

</dd> </dl>

## <a name="warning-c4311---example-1"></a>Warnung C4311-Beispiel 1

"Typumwandlung": Zeiger Verkürzung von "void \* \_ \_ ptr64" in "unsigned long"

<dl> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>Ordnung
</dt> <dd>

``` syntax
ULONG HalpMapDebugPort(
IN ULONG ComPort,
OUT PULONG ReadQva,
OUT PULONG WriteQva)
{
ULONG ComPortAddress;

ULONG PortQva;

// Compute the port address, based on the desired com port.

switch( ComPort ){
case 1:
   ComPortAddress = COM1_ISA_PORT_ADDRESS;
   break;

case 2:
default:
   ComPortAddress = COM2_ISA_PORT_ADDRESS;
}
PortQva = (ULONG)HAL_MAKE_QVA(CIA_PCI_SPARSE_IO_PHYSICAL) + ComPortAddress;

// Return the QVAs for read and write access.

*ReadQva = PortQva;
*WriteQva = PortQva;

return ComPortAddress;
}
```

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Beschreibung
</dt> <dd>

Diese gesamte Funktion behandelt Adressen als ganze Zahlen. Dies erfordert, dass die ganzen Zahlen auf tragbare Weise typiert werden müssen. Alle lokalen Variablen, Zwischenwerte in Berechnungen und Rückgabewerte sollten Portable Typen sein.

</dd> <dt>

<span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Not
</dt> <dd>

``` syntax
ULONG_PTR HalpMapDebugPort(
IN ULONG ComPort,
OUT PULONG_PTR ReadQva,
OUT PULONG_PTR WriteQva)
{
ULONG_PTR ComPortAddress;

ULONG_PTR PortQva;

// Compute the port address, based on the desired com port.

switch( ComPort ){
case 1:
   ComPortAddress = COM1_ISA_PORT_ADDRESS;
   break;

case 2:
default:
   ComPortAddress = COM2_ISA_PORT_ADDRESS;
}

PortQva = (ULONG_PTR)HAL_MAKE_QVA(CIA_PCI_SPARSE_IO_PHYSICAL) + ComPortAddress;

// Return the QVAs for read and write access.

*ReadQva = PortQva;
*WriteQva = PortQva;

return ComPortAddress;
}
```

**Pulong \_ PTR** ist ein Zeiger, der selbst 32 Bits für 32-Bit-Windows und 64 Bits für 64-Bit-Windows ist. Er verweist auf eine Ganzzahl ohne Vorzeichen, **ulong \_ ptr**, 32 Bits für 32-Bit-Windows und 64 Bits für 64-Bit-Windows.

</dd> </dl>

## <a name="warning-c4311---example-2"></a>Warnung C4311-Beispiel 2

"Typumwandlung": Zeiger Verkürzung von "void \* \_ \_ ptr64" in "unsigned long"

<dl> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>Ordnung
</dt> <dd>

``` syntax
BOOLEAN
HalpMapIoSpace (
VOID
)
{
PVOID PciIoSpaceBase;
PciIoSpaceBase = HAL_MAKE_QVA( CIA_PCI_SPARSE_IO_PHYSICAL );

//Map base addresses in QVA space.

HalpCMOSRamBase = (PVOID)((ULONG)PciIoSpaceBase + CMOS_ISA_PORT_ADDRESS);
```

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Beschreibung
</dt> <dd>

Obwohl alle QVA (quasi Virtual Address)-Werte in dieser Phase tatsächlich 32-Bit-Werte sind und in einen **ulong** passen, ist es einheitlicher, alle Adressen als **ulong \_ ptr** -Werte zu behandeln, wenn dies möglich ist.

Der Zeiger pciiospacebase enthält das QVA, das im Makro-HAL \_ make \_ QVA erstellt wird. Dieses Makro gibt einen 64-Bit-Wert zurück, bei dem die oberen 32 Bits auf 0 (null) festgelegt sind. Wir könnten einfach den Code belassen, um den Zeiger auf einen **ulong**-Wert zu kürzen, aber diese Vorgehensweise wird nicht empfohlen, um die Code Wartbarkeit und Portabilität zu verbessern. Beispielsweise kann sich der Inhalt eines QVA in der Zukunft ändern, um einige der oberen Bits auf dieser Ebene zu verwenden, und den Code zu unterbrechen.

</dd> <dt>

<span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Not
</dt> <dd>

Stellen Sie sicher, und verwenden Sie **ulong \_ ptr** für alle Adress-und Zeiger-Mathematik.

`HalpCMOSRamBase = (PVOID)((ULONG_PTR)PciIoSpaceBase + CMOS_ISA_PORT_ADDRESS);`

</dd> </dl>

## <a name="warning-c4311-example-3"></a>Warnung C4311 Beispiel 3

"Typumwandlung": Zeiger Verkürzung von "void \* \_ \_ ptr64" in "unsigned long"

<dl> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>Ordnung
</dt> <dd>

``` syntax
PVOID
HalDereferenceQva(
PVOID Qva,
INTERFACE_TYPE InterfaceType,
ULONG BusNumber)

if ( ((ULONG) Qva & QVA_SELECTORS) == QVA_ENABLE ) {

return( (PVOID)( (ULONG)Qva << IO_BIT_SHIFT ) );
} 
else {
return (Qva);
}
```

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Beschreibung
</dt> <dd>

Der Compiler warnt vor der Adresse der (&)-und Left Shift-Operatoren (<<), wenn Sie auf Zeiger Typen angewendet werden. Im obigen Code ist QVA ein **pVoid** -Wert. Dies muss in einen ganzzahligen Typ umgewandelt werden, um die Mathematik auszuführen. Da der Code portabel sein muss, verwenden Sie **ulong \_ ptr** anstelle von **ulong**.

</dd> <dt>

<span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Not
</dt> <dd>

``` syntax
if ( ((ULONG_PTR) Qva & QVA_SELECTORS) == QVA_ENABLE ) {
  return( (PVOID)( (ULONG_PTR)Qva << IO_BIT_SHIFT ) );
```

</dd> </dl>

## <a name="warning-c4311-example-4"></a>Warnung C4311 Beispiel 4

"Typumwandlung": Zeiger Verkürzung von "void \* \_ \_ ptr64" in "unsigned long"

<dl> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>Ordnung
</dt> <dd>

``` syntax
TranslatedAddress->LowPart = (ULONG)HalCreateQva(
*TranslatedAddress, va);
```

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Beschreibung
</dt> <dd>

Translatedaddress ist eine Union, die etwa wie folgt aussieht:

``` syntax
typedef union
   Struct {
      ULONG LowPart;
      LONG Highpart;
   }
   LONGLONG QuadPart;
}
```

</dd> <dt>

<span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Not
</dt> <dd>

Wenn Sie wissen, was der restliche Code in highpart platzieren könnte, können wir eine der hier gezeigten Lösungen auswählen.

`TranslatedAddress->LowPart = PtrToUlong(HalCreateQva(*TranslatedAddress,va) );`

Das **ptrtoulong** -Makro verkürzt den von **halkreateqva** zurückgegebenen Zeiger auf 32 Bits. Wir wissen, dass für das von **halkreateqva** zurückgegebene QVA die oberen 32 Bits auf NULL festgelegt sind und die nächste Zeile des Codes translatedaddress->highpart auf 0 (null) festlegt.

Mit Vorsicht können wir Folgendes verwenden:

`TranslatedAddress->QuadPart = (LONGLONG)HalCreateQva(*TranslatedAddress,va);`

Dies funktioniert in diesem Beispiel: das-Makro von **halkreateqva** gibt 64 Bits zurück, wobei die oberen 32 Bits auf 0 (null) festgelegt sind. Achten Sie darauf, dass die oberen 32 Bits nicht in einer 32-Bit-Umgebung undefiniert bleiben, was diese zweite Lösung tatsächlich bewirken könnte.

</dd> </dl>

## <a name="warning-c4311-example-5"></a>Warnung C4311 Beispiel 5

"Typumwandlung": Zeiger Verkürzung von "void \* \_ \_ ptr64" in "unsigned long"

<dl> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>Ordnung
</dt> <dd>

``` syntax
VOID
HalpCiaProgramDmaWindow(
PWINDOW_CONTROL_REGISTERS WindowRegisters,
PVOID MapRegisterBase
)
{
CIA_WBASE Wbase;

Wbase.all = 0;
Wbase.Wen = 1;
Wbase.SgEn = 1;
Wbase.Wbase = (ULONG)(WindowRegisters->WindowBase) >> 20;
```

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Beschreibung
</dt> <dd>

Windowregistern->windowbase ist ein Zeiger und ist nun 64 Bits. Der Code besagt, dass dieser Wert 20 Bits nach rechts verschiebt. Der Compiler lässt nicht zu, dass der Right Shift-Operator (>>) auf einem Zeiger verwendet wird. Daher müssen wir Sie in eine ganze Zahl umwandeln.

</dd> <dt>

<span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Not
</dt> <dd>

`Wbase.Wbase= PtrToUlong ( (PVOID) ((ULONG_PTR) (WindowRegisters->WindowBase) >> 20));`

Die Umwandlung in einen **ulong- \_ ptr** ist genau das, was wir benötigen. Das nächste Problem ist wbase. Wbase ist ein **ulong** und ist 32 Bits. In diesem Fall wissen wir, dass der 64-Bit-Zeiger windowregistern->windowbase in den niedrigeren 32 Bits auch nach dem Verschieben gültig ist. Dies verwendet das **ptrtoulong** -Makro als akzeptabel, da der 64-Bit-Zeiger in ein 32-Bit- **ulong** abgeschnitten wird. Die **pVoid** -Umwandlung ist erforderlich, da **ptrtoulong** ein Zeigerargument erwartet. Wenn Sie sich den resultierenden Assemblycode ansehen, wird die gesamte Umwandlung von C-Code nur zu einer Last von Quad, Shift Right und Store Long.

</dd> </dl>

 

 




