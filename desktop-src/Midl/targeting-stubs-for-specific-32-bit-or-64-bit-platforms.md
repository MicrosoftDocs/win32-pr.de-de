---
title: Stubziele für bestimmte 32-Bit-oder 64-Bit-Plattformen
description: Einige Features von Microsoft RPC und die Compl 3,0 und spätere Compiler sind plattformspezifisch.
ms.assetid: bb1bee56-7f39-406c-bdbf-b73bda568247
keywords:
- 32-Bit-Plattformen (Mitte)
- 64-Bit-Plattformen (Mitte)
- Stubel-Mittell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 526265a60f8b2ef2f31d19d0356d4ec3a3ae8c8f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310731"
---
# <a name="targeting-stubs-for-specific-32-bit-or-64-bit-platforms"></a><span data-ttu-id="3beaf-106">Stubziele für bestimmte 32-Bit-oder 64-Bit-Plattformen</span><span class="sxs-lookup"><span data-stu-id="3beaf-106">Targeting Stubs for Specific 32-bit or 64-bit Platforms</span></span>

<span data-ttu-id="3beaf-107">Einige Features von Microsoft RPC und die Compl 3,0 und spätere Compiler sind plattformspezifisch.</span><span class="sxs-lookup"><span data-stu-id="3beaf-107">Some of the features of Microsoft RPC and the MIDL 3.0 and later compilers are platform-specific.</span></span>

<span data-ttu-id="3beaf-108">Als Vorsichtsmaßnahme generieren die Compl 3,0-und spätere Compiler Wächter, die während der C-Kompilierungs Phase die Kompatibilitäts Überprüfung vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="3beaf-108">As a precaution, the MIDL 3.0 and later compilers generate guards that facilitate compatibility checking during the C-compilation phase.</span></span> <span data-ttu-id="3beaf-109">In der Mitte werden zwei Arten von Wächter generiert: ein Platt Form abhängiger Wächter (32-Bit und 64-Bit) und ein Freigabe abhängiger Wächter (Funktionsgruppen Abhängigkeit).</span><span class="sxs-lookup"><span data-stu-id="3beaf-109">MIDL generates two types of guards: a platform-dependent guard (32-bit versus 64-bit) and a release-dependent guard (feature set dependency).</span></span> <span data-ttu-id="3beaf-110">Beispielsweise generiert "Mittel l" den folgenden Schutz, um die C-Kompilierung eines 32-Bit-Stubs für andere Plattformen zu verhindern:</span><span class="sxs-lookup"><span data-stu-id="3beaf-110">For example, MIDL generates the following guard to prevent C-compiling of a 32-bit stub for other platforms:</span></span>

``` syntax
#if !defined(__RPC_WIN32__)
#error  Invalid build platform for this stub.
#endif
```

<span data-ttu-id="3beaf-111">Der Release-abhängige Wächter wird durch eine Reihe von Funktionen ausgelöst, die in den verarbeiteten IDL-Dateien und durch den [**/target**](-target.md) -Schalter gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="3beaf-111">The release-dependent guard is triggered by a set of features found in the processed IDL file(s) and by the [**/target**](-target.md) switch.</span></span> <span data-ttu-id="3beaf-112">Wenn die Schnittstelle z. b. Funktionen verwendet, die nur unter Windows-2000 oder höher unterstützt werden, generiert die-Schnittstelle einen Wächter mit dem Target- \_ \_ \_ Makro NT50 oder höher \_ .</span><span class="sxs-lookup"><span data-stu-id="3beaf-112">For example, if the interface uses features supported only on WindowsÂ 2000 or later, MIDL generates a guard with the TARGET\_IS\_NT50\_OR\_LATER macro.</span></span>

<span data-ttu-id="3beaf-113">Die in Rpcndr. h definierten Wächter Makros hängen von der Einstellung von WINVER und \_ Win32 \_ Winnt ab und werden vom C/C++-Compiler ausgewertet.</span><span class="sxs-lookup"><span data-stu-id="3beaf-113">The guard macros, defined in Rpcndr.h, depend on the setting of WINVER and \_WIN32\_WINNT and are evaluated by the C/C++ compiler.</span></span>

<span data-ttu-id="3beaf-114">Wenn Sie zum Zeitpunkt der C-Kompilierung eine Fehlermeldung erhalten, die besagt, dass Sie eine bestimmte Plattform zum Ausführen eines Stubs benötigen, stellen Sie zunächst sicher, dass Sie kein Feature verwendet haben, das auf dieser Plattform nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="3beaf-114">If, at C-compile time, you get an error message indicating that you need a specific platform to run a stub, first check to make sure you have not used a feature that is not available on this platform.</span></span> <span data-ttu-id="3beaf-115">Die Funktionen, die einen bestimmten Wächter auslösen, werden im Hauptteil des Schutzes aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="3beaf-115">The features triggering a particular guard are listed in the body of the guard.</span></span> <span data-ttu-id="3beaf-116">Im vorherigen Beispiel hat der-Oicf-Compilerschalter den Wächter ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="3beaf-116">In the previous example, the -Oicf compiler switch triggered the guard.</span></span> <span data-ttu-id="3beaf-117">Zu den wesentlichen Features dieser Art gehören der [**/robust**](-robust.md) -Switch und das \[ [**Async**](async.md) -Attribut, das \] unter Windows 2000 und höher verfügbar [](pipe.md) ist, der pipetypkonstruktor, die/OIF-Compileroption und die \[ Attribute [**User \_ Marshal**](user-marshal.md) \] und \[ [**Wire \_ Marshal**](wire-marshal.md) \] .</span><span class="sxs-lookup"><span data-stu-id="3beaf-117">Notable features of this kind include the [**/robust**](-robust.md) switch and the \[[**async**](async.md)\] attribute available on WindowsÂ 2000 and later, the [**pipe**](pipe.md) type constructor, the /Oif compiler option, and the \[[**user\_marshal**](user-marshal.md)\] and \[[**wire\_marshal**](wire-marshal.md)\] attributes.</span></span> <span data-ttu-id="3beaf-118">Stusb, die diese Features verwenden, werden nicht auf früheren Systemen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3beaf-118">Stubs using these features will not run on earlier systems.</span></span>

<span data-ttu-id="3beaf-119">Wenn Sie wissen, dass Ihre Zielplattform für die Features richtig ist, die Sie verwenden und weiterhin einen Fehler erhalten, müssen Sie möglicherweise die Umgebungsvariablen entsprechend festlegen.</span><span class="sxs-lookup"><span data-stu-id="3beaf-119">If you know that your target platform is correct for the features you are using and still receive an error, you may need to set the environment variables appropriately.</span></span>

<span data-ttu-id="3beaf-120">**So erstellen Sie für Windows-Versionen 2000 oder höher**</span><span class="sxs-lookup"><span data-stu-id="3beaf-120">**To build for WindowsÂ 2000 or later releases**</span></span>

-   <span data-ttu-id="3beaf-121">Fügen Sie die folgende Zeile zu Makefile hinzu:</span><span class="sxs-lookup"><span data-stu-id="3beaf-121">Add this line to your makefile:</span></span>

    ``` syntax
    CFLAGS = $(CFLAGS) -D_WIN32_WINNT=0x500
    ```

## <a name="related-topics"></a><span data-ttu-id="3beaf-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3beaf-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3beaf-123">**/Target**</span><span class="sxs-lookup"><span data-stu-id="3beaf-123">**/target**</span></span>](-target.md)
</dt> <dt>

[<span data-ttu-id="3beaf-124">**/robust**</span><span class="sxs-lookup"><span data-stu-id="3beaf-124">**/robust**</span></span>](-robust.md)
</dt> <dt>

[<span data-ttu-id="3beaf-125">**async**</span><span class="sxs-lookup"><span data-stu-id="3beaf-125">**async**</span></span>](async.md)
</dt> <dt>

[<span data-ttu-id="3beaf-126">**Async- \_ UUID**</span><span class="sxs-lookup"><span data-stu-id="3beaf-126">**async\_uuid**</span></span>](async-uuid.md)
</dt> <dt>

[<span data-ttu-id="3beaf-127">**/Oi**</span><span class="sxs-lookup"><span data-stu-id="3beaf-127">**/Oi**</span></span>](-oi.md)
</dt> <dt>

[<span data-ttu-id="3beaf-128">**Kanal**</span><span class="sxs-lookup"><span data-stu-id="3beaf-128">**pipe**</span></span>](pipe.md)
</dt> <dt>

[<span data-ttu-id="3beaf-129">**Wire \_ Marshal**</span><span class="sxs-lookup"><span data-stu-id="3beaf-129">**wire\_marshal**</span></span>](wire-marshal.md)
</dt> <dt>

[<span data-ttu-id="3beaf-130">**Benutzer \_ Mars Hall**</span><span class="sxs-lookup"><span data-stu-id="3beaf-130">**user\_marshal**</span></span>](user-marshal.md)
</dt> <dt>

[<span data-ttu-id="3beaf-131">Marshalling von OLE-Datentypen</span><span class="sxs-lookup"><span data-stu-id="3beaf-131">Marshaling OLE Data Types</span></span>](marshaling-ole-data-types.md)
</dt> </dl>

 

 




