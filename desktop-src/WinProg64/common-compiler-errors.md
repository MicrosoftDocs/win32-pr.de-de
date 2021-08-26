---
title: Häufige Compilerfehler
description: In diesem Abschnitt werden die typischen Compilerfehler veranschaulicht, die beim Migrieren einer vorhandenen Codebasis auftreten. Diese Beispiele kommen aus DEM SYSTEM-Code auf Systemebene, obwohl die Konzepte direkt auf Code auf Benutzerebene anwendbar sind.
ms.assetid: bbb6a57f-281a-4a6e-a4b6-15846d0cf21f
keywords:
- Compilerfehler 64-Bit-Windows Programmierung
- Migration von 64-Bit-Windows Programmierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55d12e7c5566b5cb2b934eefb71b1b51858f278d3e408d3080cb1810f185dcfb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071640"
---
# <a name="common-compiler-errors"></a>Häufige Compilerfehler

In diesem Abschnitt werden die typischen Compilerfehler veranschaulicht, die beim Migrieren einer vorhandenen Codebasis auftreten. Diese Beispiele kommen aus DEM SYSTEM-Code auf Systemebene, obwohl die Konzepte direkt auf Code auf Benutzerebene anwendbar sind.

## <a name="warning-c4311-example-1"></a>Warnung C4311 Beispiel 1

'Typ cast': Zeigerabschneidung von 'void \* \_ \_ ptr64' auf 'unsigned long'

<dl> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>Code
</dt> <dd>

`pPciAddr->u.AsULONG = (ULONG) CIA_PCI_CONFIG_BASE_QVA;`

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Beschreibung
</dt> <dd>

**PtrToUlong ist** abhängig von Ihrer Verwendung eine Inlinefunktion oder ein Makro. Sie schneide einen Zeiger auf ein **ULONG--Schneidefeld ab.** Obwohl 32-Bit-Zeiger nicht betroffen sind, wird die obere Hälfte eines 64-Bit-Zeigers abgeschnitten.

CIA \_ PCI \_ CONFIG BASE \_ \_ QVA ist als **PVOID deklariert.** Die **ULONG-Cast** funktioniert in der 32-Bit-Welt, führt jedoch in der 64-Bit-Welt zu einem Fehler. Die Lösung besteht im Erhalten eines 64-Bit-Zeigers auf **einen ULONG,** da das Ändern der Definition der Union, die pPciAddr->u.AsULONG definiert ist, zu viel Code ändert.

Die Verwendung des **PtrToUlong-Makros** zum Konvertieren des 64-Bit-PVOID in die benötigte **ULONG** ist zulässig, da wir über Informationen zum spezifischen Wert der CIA PCI  \_ \_ CONFIG BASE \_ \_ QVA verfügen. In diesem Fall hat dieser Zeiger nie Daten in den oberen 32 Bits.

</dd> <dt>

<span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Lösung
</dt> <dd>

`pPciAddr->u.AsULONG = PtrToUlong(CIA_PCI_CONFIG_BASE_QVA);`

</dd> </dl>

## <a name="warning-c4311-example-2"></a>Warnung C4311 Beispiel 2

'typ cast': Zeigerabschneidung von \_ 'StrukturFEHLER \_ FRAME \* \_ \_ ptr64 ' auf 'unsigned long'

<dl> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>Code
</dt> <dd>

`KeBugCheckEx( DATA_BUS_ERROR,0,0,0,(ULONG)PUncorrectableError );`

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Beschreibung
</dt> <dd>

Das Problem ist, dass der letzte Parameter für diese Funktion ein Zeiger auf eine Datenstruktur ist. Da PUncorrectableError ein Zeiger ist, ändert sich die Größe mit dem Programmiermodell. Der Prototyp für **KeBugCheckEx** wurde geändert, sodass der letzte Parameter ein **ULONG \_ PTR ist.** Daher ist es erforderlich, den Funktionszeiger in einen **ULONG \_ PTR zu casten.**

Sie können fragen, **warum PVOID** nicht als letzter Parameter verwendet wurde. Je nach Kontext des Aufrufs kann der letzte Parameter etwas anderes als ein Zeiger oder möglicherweise ein Fehlercode sein.

</dd> <dt>

<span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Lösung
</dt> <dd>

`KeBugCheckEx( DATA_BUS_ERROR,0,0,0,(ULONG_PTR)PUncorrectableError );`

</dd> </dl>

## <a name="warning-c4244-example-1"></a>Warnung C4244 Beispiel 1

'=': Konvertierung von 'struct \_ CONFIGURATION \_ COMPONENT \* \_ \_ ptr64 ' in 'struct CONFIGURATION COMPONENT \_ \_ \* ', möglicher Datenverlust

<dl> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>Code
</dt> <dd>

`Component = &CurrentEntry->ComponentEntry;`

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Beschreibung
</dt> <dd>

Die Funktion deklariert die Variable Component als PCONFIGURATION \_ COMPONENT. Später wird die Variable in der folgenden Zuweisung verwendet, die korrekt erscheint:

`Component = &CurrentEntry->ComponentEntry;`

Der Typ PCONFIGURATION \_ COMPONENT ist jedoch wie im folgenden Beispiel definiert:

``` syntax
typedef struct __CONFIGURATION_COMPONENT {
...
...
} CONFIGURATION_COMPONENT, * POINTER_32 PCONFIGURATION_COMPONENT;
```

Die Typdefinition für PCONFIGURATION COMPONENT bietet einen \_ 32-Bit-Zeiger in 32-Bit- und 64-Bit-Modellen, da sie **als POINTER \_ 32** deklariert ist. Der ursprüngliche Designer dieser Struktur wusste, dass sie in einem 32-Bit-Kontext im BIOS verwendet und für diese Verwendung ausdrücklich definiert wurde. Dieser Code funktioniert in 32-Bit-Windows, da die Zeiger 32-Bit sind. In 64-Bit-Windows funktioniert dies nicht, da sich der Code im 64-Bit-Kontext befindet.

</dd> <dt>

<span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Lösung
</dt> <dd>

Um dieses Problem zu beheben, verwenden Sie CONFIGURATION \_ COMPONENT \* anstelle der 32-Bit-PCONFIGURATION \_ COMPONENT. Es ist wichtig, den Zweck des Codes klar zu verstehen. Wenn dieser Code zum Berühren des 32-Bit-BIOS oder des Systemraums vorgesehen ist, funktioniert diese Korrektur nicht.

**POINTER \_ 32** ist in Ntdef.h und Winnt.h definiert.

``` syntax
#ifdef (__AXP64__)
#define POINTER_32 _ptr32
#else
#define POINTER_32
#endif
```

</dd> </dl>

## <a name="warning-c4242-example-2"></a>Warnung C4242 Beispiel 2

'=': Konvertierung von ' \_ \_ int64 ' in 'unsigned long ', möglicher Datenverlust

<dl> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>Code
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

Diese Warnung wird generiert, da die Berechnung 64-Bit-Werte verwendet, in diesem Fall Zeiger, und das Ergebnis in einem 32-Bit-ULONG-Wert **platziert.**

</dd> <dt>

<span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Lösung
</dt> <dd>

Typ cast the result of the calculation to a **ULONG** as shown here:

`ByteSelect1 = (ULONG)(NvDestPtr - (PUCHAR)HalpCMOSRamBase) & CONFIG_RAM_BYTE_MASK;`

Durch Die Typcastung des Ergebnisses wird dem Compiler bekannt, dass Sie sich über das Ergebnis sicher sind. Stellen Sie jedoch sicher, dass Sie die Berechnung verstehen und sicher sind, dass sie in eine 32-Bit-ULONG **passt.**

Wenn das Ergebnis möglicherweise nicht in eine 32-Bit-ULONG-Umgebung passt, ändern Sie den Basistyp der Variablen, die das Ergebnis in sich hat.

</dd> </dl>

## <a name="warning-c4311---example-1"></a>Warnung C4311 – Beispiel 1

'typ cast': Zeigerabschneidung von 'void \* \_ \_ ptr64 ' auf 'unsigned long '

<dl> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>Code
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

Diese gesamte Funktion behandelt Adressen als ganze Zahlen, was es erforderlich machen muss, diese ganzen Zahlen portabel eingibt. Alle lokalen Variablen, Zwischenwerte in Berechnungen und Rückgabewerte sollten portable Typen sein.

</dd> <dt>

<span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Lösung
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

**PULONG \_ PTR** ist ein Zeiger, der selbst 32 Bits für 32-Bit-Windows und 64 Bit für 64-Bit-Windows. Er verweist auf eine ganze Zahl ohne Vorzeichen, **ULONG \_ PTR,** die 32 Bits für 32-Bit-Windows und 64 Bits für 64-Bit-Windows.

</dd> </dl>

## <a name="warning-c4311---example-2"></a>Warnung C4311 – Beispiel 2

'typ cast': Zeigerabschneidung von 'void \* \_ \_ ptr64 ' auf 'unsigned long '

<dl> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>Code
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

Obwohl alle QVA-Werte (Quasi Virtual Address) zu diesem Zeitpunkt tatsächlich 32-Bit-Werte sind und in **ULONG** passen, ist es konsistenter, alle Adressen nach Möglichkeit als **ULONG \_ PTR-Werte** zu behandeln.

Der Zeiger PciIoSpaceBase enthält das QVA, das im Makro PCI \_ MAKE \_ QVA erstellt wird. Dieses Makro gibt einen 64-Bit-Wert zurück, bei dem die obersten 32 Bits auf 0 (null) festgelegt sind, damit die Mathematik funktioniert. Wir könnten den Code einfach so bewenden, dass der Zeiger in einem **ULONG** abgeschnitten wird, aber von dieser Vorgehensweise wird abgeraten, um die Wartbarkeit und Portabilität von Code zu verbessern. Beispielsweise kann sich der Inhalt eines QVA in Zukunft ändern, um einige der oberen Bits auf dieser Ebene zu verwenden, was den Code unterbricht.

</dd> <dt>

<span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Lösung
</dt> <dd>

Seien Sie sicher, und verwenden **Sie ULONG \_ PTR** für alle Mathematischen Adressen und Zeiger.

`HalpCMOSRamBase = (PVOID)((ULONG_PTR)PciIoSpaceBase + CMOS_ISA_PORT_ADDRESS);`

</dd> </dl>

## <a name="warning-c4311-example-3"></a>Warnung C4311 Beispiel 3

'typ cast': Zeigerabschneidung von 'void \* \_ \_ ptr64 ' auf 'unsigned long '

<dl> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>Code
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

Der Compiler warnt vor der Adresse von Operatoren (&) und Linksverschiebungsoperatoren (<<), wenn sie auf Zeigertypen angewendet werden. Im obigen Code ist Qva ein **PVOID-Wert.** Wir müssen dies in einen ganzzahligen Typ konvertieren, um die Mathematik durchzuführen. Da der Code portabel sein muss, verwenden Sie **ULONG \_ PTR** anstelle **von ULONG**.

</dd> <dt>

<span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Lösung
</dt> <dd>

``` syntax
if ( ((ULONG_PTR) Qva & QVA_SELECTORS) == QVA_ENABLE ) {
  return( (PVOID)( (ULONG_PTR)Qva << IO_BIT_SHIFT ) );
```

</dd> </dl>

## <a name="warning-c4311-example-4"></a>Warnung C4311 Beispiel 4

'typ cast': Zeigerabschneidung von 'void \* \_ \_ ptr64 ' auf 'unsigned long '

<dl> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>Code
</dt> <dd>

``` syntax
TranslatedAddress->LowPart = (ULONG)HalCreateQva(
*TranslatedAddress, va);
```

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Beschreibung
</dt> <dd>

TranslatedAddress ist eine Union, die in etwa wie folgt aussieht:

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

<span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Lösung
</dt> <dd>

Wenn Wir wissen, was der restliche Code in Highpart platzieren könnte, können wir eine der hier gezeigten Lösungen auswählen.

`TranslatedAddress->LowPart = PtrToUlong(HalCreateQva(*TranslatedAddress,va) );`

Das **PtrToUlong-Makro** schneide den zeiger, der **vonCreateQva** zurückgegeben wird, auf 32 Bits ab. Wir wissen, dass für das QVA, das **von PerlCreateQva** zurückgegeben wird, die oberen 32 Bits auf 0 festgelegt sind, und dass die nächste Codezeile TranslatedAddress->Highpart auf 0 (null) setzt.

Mit Vorsicht könnten wir Folgendes verwenden:

`TranslatedAddress->QuadPart = (LONGLONG)HalCreateQva(*TranslatedAddress,va);`

Dies funktioniert in diesem Beispiel: Das **Makro "HalogenCreateQva"** gibt 64 Bits zurück, und die oberen 32 Bits sind auf 0 (null) festgelegt. Achten Sie darauf, die oberen 32 Bits nicht in einer 32-Bit-Umgebung undefiniert zu lassen, was diese zweite Lösung tatsächlich tun kann.

</dd> </dl>

## <a name="warning-c4311-example-5"></a>Warnung C4311 Beispiel 5

'typ cast': Zeigerkürzung von 'void \* \_ \_ ptr64' auf 'unsigned long '

<dl> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>Code
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

WindowRegisters->WindowBase ist ein Zeiger und hat jetzt 64 Bits. Der Code besagt, dass dieser Wert um 20 Bits nach rechts verschoben werden soll. Der Compiler lässt uns die Verwendung des Rechtsschiebeoperators (>>) für einen Zeiger nicht zu. daher müssen wir sie in eine Art ganzzahlige Zahl umsetzen.

</dd> <dt>

<span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Lösung
</dt> <dd>

`Wbase.Wbase= PtrToUlong ( (PVOID) ((ULONG_PTR) (WindowRegisters->WindowBase) >> 20));`

Die Umwandlung in eine **ULONG \_ PTR** ist genau das, was wir benötigen. Das nächste Problem ist Wbase. Wbase ist ein **ULONG** und 32 Bits. In diesem Fall wissen wir, dass der 64-Bit-Zeiger WindowRegisters->WindowBase auch nach der Verschiebung in den unteren 32 Bits gültig ist. Dadurch wird die Verwendung des **PtrToUlong-Makros** akzeptabel, da es den 64-Bit-Zeiger in eine 32-Bit-ULONG abschneidet.  Die **PVOID-Umwandlung** ist erforderlich, da **PtrToUlong** ein Zeigerargument erwartet. Wenn Sie sich den resultierenden Assemblercode ansehen, wird all diese C-Codeumwandelung nur zu einem Ladequad quad, nach rechts verschoben und lang gespeichert.

</dd> </dl>

 

 




