---
title: /version_stamp Schalter
description: Der Schalter "/Version Stamp" unter \_ drückt die Generierung von Makros, die die mindestens erforderliche Versionsnummer der RPC-Header Datei "Rpcndr. h" angeben.
ms.assetid: ec03f68b-60f7-431e-9fba-4434ef082058
keywords:
- /version_stamp-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /version_stamp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 704393dce869df4e5f715a1157cdb57967135e42
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "106338029"
---
# <a name="version_stamp-switch"></a><span data-ttu-id="dcb11-104">/Version \_ Stamp-Schalter</span><span class="sxs-lookup"><span data-stu-id="dcb11-104">/version\_stamp switch</span></span>

<span data-ttu-id="dcb11-105">Der Schalter " **/Version \_ Stamp** " unterdrückt die Generierung von Makros, die die mindestens erforderliche Versionsnummer der RPC-Header Datei "Rpcndr. h" angeben.</span><span class="sxs-lookup"><span data-stu-id="dcb11-105">The **/version\_stamp** switch suppresses the generation of macros that specify the minimum required version number of the RPC header file, Rpcndr.h.</span></span>

<span data-ttu-id="dcb11-106">Neue Mittelwert Funktionen erfordern möglicherweise zusätzliche Definitionen, um den Stub ordnungsgemäß zu kompilieren. der Stub verfügt daher über Makros, die die Kompatibilität zwischen den mittleren Binärdateien und der Buildumgebung überprüfen.</span><span class="sxs-lookup"><span data-stu-id="dcb11-106">New MIDL features might require additional definitions to compile the stub correctly, so the stub has macros that check compatibility between MIDL binary files and the build environment.</span></span> <span data-ttu-id="dcb11-107">Möglicherweise müssen Sie diesen Schalter verwenden, wenn Sie die mittlere Größe in eine andere Buildumgebung verschieben, als die, in der Sie zunächst die mittleren Binärdateien installiert haben.</span><span class="sxs-lookup"><span data-stu-id="dcb11-107">You might need to use this switch if you move MIDL to a different build environment than the one in which you first installed the MIDL binary files.</span></span>

<span data-ttu-id="dcb11-108">Beachten Sie, dass das Mischen von Buildumgebungen nicht unterstützt wird</span><span class="sxs-lookup"><span data-stu-id="dcb11-108">Note that mixing build environments is not supported.</span></span>

``` syntax
midl /version_stamp
```

## <a name="switch-options"></a><span data-ttu-id="dcb11-109">Optionen wechseln</span><span class="sxs-lookup"><span data-stu-id="dcb11-109">Switch Options</span></span>

<span data-ttu-id="dcb11-110">Dieser Switch hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="dcb11-110">This switch has no parameters.</span></span>

 

 




