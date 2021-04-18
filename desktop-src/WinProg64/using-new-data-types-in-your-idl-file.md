---
title: Verwenden neuer Datentypen in ihrer IDL-Datei
description: Die Header Datei "basetsd. h" definiert die neuen Datentypen, die zum Schreiben von Anwendungen benötigt werden, die sowohl unter 32-als auch 64-Bit-Windows ausgeführt werden.
ms.assetid: 99a3904b-9120-4d1d-bd8c-1eb299bd6b27
keywords:
- Basetsd. h-Header Datei 64-Bit-Windows-Programmierung
- Datentypen in der IDL-Datei 64-Bit-Windows-Programmierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ff1add2d70c99069911ac76ad168b7d31c3365f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106337655"
---
# <a name="using-new-data-types-in-your-idl-file"></a><span data-ttu-id="7e2b2-105">Verwenden neuer Datentypen in ihrer IDL-Datei</span><span class="sxs-lookup"><span data-stu-id="7e2b2-105">Using New Data Types in Your IDL File</span></span>

<span data-ttu-id="7e2b2-106">Die Header Datei "basetsd. h" definiert die neuen Datentypen, die zum Schreiben von Anwendungen benötigt werden, die sowohl unter 32-als auch 64-Bit-Windows ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="7e2b2-106">The Basetsd.h header file defines the new data types needed for writing applications that run on both 32- and 64-bit Windows.</span></span> <span data-ttu-id="7e2b2-107">Um diese Datentypen in ihren Schnittstellen zu verwenden, importieren Sie basetsd. h in Ihre IDL-Datei.</span><span class="sxs-lookup"><span data-stu-id="7e2b2-107">To use these data types in your interfaces, import Basetsd.h into your IDL file.</span></span> <span data-ttu-id="7e2b2-108">\#Schließen Sie die Datei nicht ein, oder es werden mehrere Definitionen zum Zeitpunkt der Kompilierung erstellt.</span><span class="sxs-lookup"><span data-stu-id="7e2b2-108">Do not \#include the file or you will end up with multiple definitions at compile time.</span></span>

<span data-ttu-id="7e2b2-109">Alternativ dazu können Sie die Datei "basetsd. idl" in Ihre IDL-Datei einschließen oder importieren.</span><span class="sxs-lookup"><span data-stu-id="7e2b2-109">Alternatively, you can include or import the Basetsd.idl file into your IDL file.</span></span>

<span data-ttu-id="7e2b2-110">Weitere Informationen zum Hinzufügen von System Header Dateien zu ihrer IDL-Datei finden Sie unter [Importieren von Dateien und Typbibliotheken](/windows/desktop/Midl/importing-files-and-type-libraries) und [Importieren von System Header Dateien](/windows/desktop/Midl/importing-system-header-files).</span><span class="sxs-lookup"><span data-stu-id="7e2b2-110">For more information on adding system header files to your IDL file, see [Importing Files and Type Libraries](/windows/desktop/Midl/importing-files-and-type-libraries) and [Importing System Header Files](/windows/desktop/Midl/importing-system-header-files).</span></span>

 

 