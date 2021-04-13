---
title: Fehlerbehandlung in com (com)
description: Fehlerbehandlung in com
ms.assetid: 15f3ae3e-1794-4948-a7aa-6309a703364b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19af496eabf50833c99d462ff074254bc39bb7a0
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104475009"
---
# <a name="error-handling-in-com-com"></a><span data-ttu-id="cce05-103">Fehlerbehandlung in com (com)</span><span class="sxs-lookup"><span data-stu-id="cce05-103">Error Handling in COM (COM)</span></span>

<span data-ttu-id="cce05-104">Fast alle com-Funktionen und Schnittstellen Methoden geben einen Wert vom Typ **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="cce05-104">Almost all COM functions and interface methods return a value of the type **HRESULT**.</span></span> <span data-ttu-id="cce05-105">Das **HRESULT** (für das *Ergebnis Handle*) ist eine Möglichkeit, Erfolgs-, Warnungs-und Fehler Werte zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="cce05-105">The **HRESULT** (for *result handle*) is a way of returning success, warning, and error values.</span></span> <span data-ttu-id="cce05-106">**HRESULT** s werden für nichts behandelt. Dabei handelt es sich nur um Werte, deren Felder im-Wert codiert sind.</span><span class="sxs-lookup"><span data-stu-id="cce05-106">**HRESULT** s are really not handles to anything; they are only values with several fields encoded in the value.</span></span> <span data-ttu-id="cce05-107">Gemäß der com-Spezifikation gibt das Ergebnis 0 (null) einen Erfolg an, und ein Ergebnis ungleich NULL weist auf einen Fehler hin.</span><span class="sxs-lookup"><span data-stu-id="cce05-107">As per the COM specification, a result of zero indicates success and a nonzero result indicates failure.</span></span>

<span data-ttu-id="cce05-108">Auf Quell Code Ebene bestehen alle Fehler Werte aus drei Teilen, die durch Unterstriche voneinander getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="cce05-108">At the source code level, all error values consist of three parts, separated by underscores.</span></span> <span data-ttu-id="cce05-109">Der erste Teil ist das Präfix, das die dem Fehler zugeordnete Anlage identifiziert, der zweite Teil "E" für "Error" und der dritte Teil eine Zeichenfolge, die die tatsächliche Bedingung beschreibt.</span><span class="sxs-lookup"><span data-stu-id="cce05-109">The first part is the prefix that identifies the facility associated with the error, the second part is E for error, and the third part is a string that describes the actual condition.</span></span> <span data-ttu-id="cce05-110">Beispielsweise wird **STG \_ E \_ mediüberfull** zurückgegeben, wenn auf einer Festplatte kein Speicherplatz mehr vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="cce05-110">For example, **STG\_E\_MEDIUMFULL** is returned when there is no space left on a hard disk.</span></span> <span data-ttu-id="cce05-111">Das **STG** -Präfix gibt den Speicherplatz an, der **E** gibt an, dass der Statuscode einen Fehler darstellt und der **mediumfull** bestimmte Informationen über den Fehler enthält.</span><span class="sxs-lookup"><span data-stu-id="cce05-111">The **STG** prefix indicates the storage facility, the **E** indicates that the status code represents an error, and the **MEDIUMFULL** provides specific information about the error.</span></span> <span data-ttu-id="cce05-112">Viele der Werte, die Sie möglicherweise von einer Schnittstellen Methode oder Funktion zurückgeben möchten, sind in WinError. h definiert.</span><span class="sxs-lookup"><span data-stu-id="cce05-112">Many of the values that you might want to return from an interface method or function are defined in Winerror.h.</span></span>

<span data-ttu-id="cce05-113">Weitere Informationen zur Fehlerbehandlung finden Sie in den folgenden Abschnitten:</span><span class="sxs-lookup"><span data-stu-id="cce05-113">For more information about error handling, see the following sections:</span></span>

-   [<span data-ttu-id="cce05-114">Struktur von com-Fehler Codes</span><span class="sxs-lookup"><span data-stu-id="cce05-114">Structure of COM Error Codes</span></span>](structure-of-com-error-codes.md)
-   [<span data-ttu-id="cce05-115">Codes in der \_ Einrichtung der Einrichtung</span><span class="sxs-lookup"><span data-stu-id="cce05-115">Codes in FACILITY\_ITF</span></span>](codes-in-facility-itf.md)
-   [<span data-ttu-id="cce05-116">Verwenden von Makros für die Fehlerbehandlung</span><span class="sxs-lookup"><span data-stu-id="cce05-116">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)
-   [<span data-ttu-id="cce05-117">COM-Fehlerbehandlung in Java und Visual Basic</span><span class="sxs-lookup"><span data-stu-id="cce05-117">COM Error Handling in Java and Visual Basic</span></span>](com-error-handling-in-java-and-visual-basic.md)
-   [<span data-ttu-id="cce05-118">Fehlerbehandlungsstrategien</span><span class="sxs-lookup"><span data-stu-id="cce05-118">Error Handling Strategies</span></span>](error-handling-strategies.md)
-   [<span data-ttu-id="cce05-119">Behandeln von unbekannten Fehlern</span><span class="sxs-lookup"><span data-stu-id="cce05-119">Handling Unknown Errors</span></span>](handling-unknown-errors.md)

## <a name="related-topics"></a><span data-ttu-id="cce05-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="cce05-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cce05-121">COM-Fehler Codes</span><span class="sxs-lookup"><span data-stu-id="cce05-121">COM Error Codes</span></span>](com-error-codes.md)
</dt> </dl>

 

 




