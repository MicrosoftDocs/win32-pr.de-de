---
title: /savePP-Schalter
description: Wenn die/savePP-Direktive angegeben wird, löscht der mittlerer l-Compiler nicht die Ausgabe des C/C++-Präprozessors.
ms.assetid: 65a687a5-55ec-4e76-bcfc-38c0a317b85b
keywords:
- /savePP-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /savePP
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5d3ab7032768cacfab6415548a09def453ab4f9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104038007"
---
# <a name="savepp-switch"></a><span data-ttu-id="57106-104">/savePP-Schalter</span><span class="sxs-lookup"><span data-stu-id="57106-104">/savePP switch</span></span>

<span data-ttu-id="57106-105">Wenn die **/savePP** -Direktive angegeben wird, löscht der mittlerer l-Compiler nicht die Ausgabe des C/C++-Präprozessors.</span><span class="sxs-lookup"><span data-stu-id="57106-105">When the **/savePP** directive is specified, the MIDL compiler does not delete the output of the C/C++ preprocessor.</span></span>

``` syntax
midl /savePP
```

## <a name="switch-options"></a><span data-ttu-id="57106-106">Optionen wechseln</span><span class="sxs-lookup"><span data-stu-id="57106-106">Switch Options</span></span>

<span data-ttu-id="57106-107">Dieser Switch hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="57106-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="57106-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="57106-108">Remarks</span></span>

<span data-ttu-id="57106-109">Mithilfe dieses Schalters können Entwickler erkennen, was vom Mittelwert Compiler analysiert wird, und sind für das Debuggen nützlich.</span><span class="sxs-lookup"><span data-stu-id="57106-109">This switch enables developers to discern what is being parsed by the MIDL compiler, and is useful for debugging.</span></span> <span data-ttu-id="57106-110">Die Ausgabe des Präprozessors wird in eine oder mehrere temporäre Dateien in dem Verzeichnis geschrieben, das von der TEMP-Umgebungsvariablen angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="57106-110">The output of the preprocessor is written to one or more temporary files in the directory indicated by the TEMP environment variable.</span></span> <span data-ttu-id="57106-111">Der Name der Ausgabedatei (oder Dateien) folgt einer Benennungs Konvention von Mid \* . tmp.</span><span class="sxs-lookup"><span data-stu-id="57106-111">The name of the output file, or files, follows a naming convention of MID\*.tmp.</span></span> <span data-ttu-id="57106-112">Beachten Sie, dass bei einer einzelnen Kompilierung mehrere vorverarbeitete Eingabedaten Ströme generiert werden können. Dies liegt daran, dass das Importieren einer IDL-Datei im Gegensatz zur Verwendung von **\# include** eine separate präprozessorlaufzeit bewirkt.</span><span class="sxs-lookup"><span data-stu-id="57106-112">Note that a single compile may generate several preprocessed input streams; this is because importing an IDL file, as opposed to using **\#include**, causes a separate preprocessor run.</span></span>

## <a name="see-also"></a><span data-ttu-id="57106-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="57106-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57106-114">**/cpp- \_ cmd**</span><span class="sxs-lookup"><span data-stu-id="57106-114">**/cpp\_cmd**</span></span>](-cpp-cmd.md)
</dt> <dt>

[<span data-ttu-id="57106-115">**/cpp \_ Opt**</span><span class="sxs-lookup"><span data-stu-id="57106-115">**/cpp\_opt**</span></span>](-cpp-opt.md)
</dt> <dt>

[<span data-ttu-id="57106-116">/No \_ cpp,/nocpp</span><span class="sxs-lookup"><span data-stu-id="57106-116">/no\_cpp, /nocpp</span></span>](-no-cpp-nocpp.md)
</dt> </dl>

 

 




