---
description: Verarbeiten von Unicode in einer IME-Aware Anwendung
ms.assetid: fa202c1e-d0af-441f-b878-ed98205a880c
title: Verarbeiten von Unicode in einer IME-Aware Anwendung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d78174776eb608c3e494fd5967acba41609e436a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349717"
---
# <a name="handling-unicode-in-an-ime-aware-application"></a><span data-ttu-id="43e61-103">Verarbeiten von Unicode in einer IME-Aware Anwendung</span><span class="sxs-lookup"><span data-stu-id="43e61-103">Handling Unicode in an IME-Aware Application</span></span>

<span data-ttu-id="43e61-104">Mit dem imm und der Handhabung von Unicode sind zwei Probleme verbunden.</span><span class="sxs-lookup"><span data-stu-id="43e61-104">Two issues are involved with the IMM and its handling of Unicode.</span></span> <span data-ttu-id="43e61-105">Das erste Problem besteht darin, dass die Unicode-Versionen der imm-Funktionen die Größe eines Puffers in Bytes anstelle von 16-Bit-Unicode-Zeichen abrufen.</span><span class="sxs-lookup"><span data-stu-id="43e61-105">The first issue is that the Unicode versions of IMM functions retrieve the size of a buffer in bytes instead of 16-bit Unicode characters.</span></span> <span data-ttu-id="43e61-106">Das zweite Problem besteht darin, dass der imm normalerweise Unicode-Zeichen (anstelle von DBCS-Zeichen) in den Zeichen Nachrichten [**WM \_ char**](../inputdev/wm-char.md) und [**WM \_ IME \_**](wm-ime-char.md) abruft.</span><span class="sxs-lookup"><span data-stu-id="43e61-106">The second issue is that the IMM normally retrieves Unicode characters (instead of DBCS characters) in the [**WM\_CHAR**](../inputdev/wm-char.md) and [**WM\_IME\_CHAR**](wm-ime-char.md) messages.</span></span>

<span data-ttu-id="43e61-107">Windows unterstützt eine Unicode-Schnittstelle für das IMM, zusätzlich zur ursprünglich unterstützten ANSI-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="43e61-107">Windows supports a Unicode interface for the IMM, in addition to the ANSI interface originally supported.</span></span>

<span data-ttu-id="43e61-108">Ihre Anwendungen sollten [**registerclassw**](/windows/win32/api/winuser/nf-winuser-registerclassa) verwenden, damit die " [**WM \_ char**](../inputdev/wm-char.md) "-und " [**WM IME"- \_ \_ char**](wm-ime-char.md) -Nachrichten anstelle von DBCS-Zeichen im *wParam* -Parameter Unicode-Zeichen abrufen können.</span><span class="sxs-lookup"><span data-stu-id="43e61-108">Your applications should use [**RegisterClassW**](/windows/win32/api/winuser/nf-winuser-registerclassa) to cause the [**WM\_CHAR**](../inputdev/wm-char.md) and [**WM\_IME\_CHAR**](wm-ime-char.md) messages to retrieve Unicode characters instead of DBCS characters in the *wParam* parameter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="43e61-109">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="43e61-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43e61-110">Verwenden des Eingabemethoden-Managers</span><span class="sxs-lookup"><span data-stu-id="43e61-110">Using Input Method Manager</span></span>](using-input-method-manager.md)
</dt> </dl>

 

 
