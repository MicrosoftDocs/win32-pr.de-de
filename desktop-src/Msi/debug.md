---
description: Wenn diese pro-Computer-System Richtlinie auf &\# 0034; 1&0034; festgelegt ist \# , schreibt der Installer gängige Debugmeldungen mithilfe der OutputDebugString-Funktion in den Debugger.
ms.assetid: 0a9416ca-0535-4595-a4f3-b3ef7c2d3a13
title: Debuggen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2615b12bb76f4c4da0677bbeb459fa549f8233e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866363"
---
# <a name="debug"></a><span data-ttu-id="732c2-103">Debuggen</span><span class="sxs-lookup"><span data-stu-id="732c2-103">Debug</span></span>

<span data-ttu-id="732c2-104">Wenn diese pro-Computer- [System Richtlinie](system-policy.md) auf "1" festgelegt ist, schreibt der Installer gängige Debugmeldungen mithilfe der [**OutputDebugString**](/windows/desktop/api/debugapi/nf-debugapi-outputdebugstringw) -Funktion in den Debugger.</span><span class="sxs-lookup"><span data-stu-id="732c2-104">If this per-machine [system policy](system-policy.md) is set to "1", the installer writes common debugging messages to the debugger using the [**OutputDebugString**](/windows/desktop/api/debugapi/nf-debugapi-outputdebugstringw) function.</span></span> <span data-ttu-id="732c2-105">Wenn dieser Wert auf "2" festgelegt ist, schreibt das Installationsprogramm mit der [**OutputDebugString**](/windows/desktop/api/debugapi/nf-debugapi-outputdebugstringw) -Funktion alle gültigen Debugmeldungen in den Debugger.</span><span class="sxs-lookup"><span data-stu-id="732c2-105">If this value is set to "2", the installer writes all valid debugging messages to the debugger using the [**OutputDebugString**](/windows/desktop/api/debugapi/nf-debugapi-outputdebugstringw) function.</span></span> <span data-ttu-id="732c2-106">Diese Richtlinie dient nur zu Debuggingzwecken und wird in zukünftigen Versionen von Windows Installer möglicherweise nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="732c2-106">This policy is for debugging purposes only and may not be supported in future versions of Windows Installer.</span></span>

<span data-ttu-id="732c2-107">Windows Installer schreibt Befehlszeilen nur in die Protokolldatei, wenn das dritte (0x04) Bit im Wert der debugrichtlinie festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="732c2-107">Windows Installer only writes command lines into the log file if the third (0x04) bit is set in the value of the Debug policy.</span></span> <span data-ttu-id="732c2-108">Um Befehlszeilen im Protokoll anzuzeigen, legen Sie den Wert der Debug-Richtlinie daher auf 7 fest.</span><span class="sxs-lookup"><span data-stu-id="732c2-108">Therefore, to display command lines in the log, set the Debug policy value to 7.</span></span> <span data-ttu-id="732c2-109">Dadurch werden keine Eigenschaften angezeigt, die einem [Bearbeitungs Steuer](edit-control.md) Element zugeordnet sind, das über das Kenn [Wort Steuerungs Attribut](password-control-attribute.md)verfügt.</span><span class="sxs-lookup"><span data-stu-id="732c2-109">This does not display properties associated with an [Edit Control](edit-control.md) having the [Password Control Attribute](password-control-attribute.md).</span></span> <span data-ttu-id="732c2-110">Dadurch werden die Eigenschaften, die in der Befehlszeile angezeigt werden, im Protokoll angezeigt, auch wenn die Eigenschaft in der [**msihiddenproperties**](msihiddenproperties.md) -Eigenschaft enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="732c2-110">This will make properties set on the command line visible in the log even if the property is included in the [**MsiHiddenProperties**](msihiddenproperties.md) property.</span></span> <span data-ttu-id="732c2-111">Weitere Informationen finden Sie unter [verhindern, dass vertrauliche Informationen in die Protokolldatei geschrieben werden](preventing-confidential-information-from-being-written-into-the-log-file.md).</span><span class="sxs-lookup"><span data-stu-id="732c2-111">For more information, see [Preventing Confidential Information from Being Written into the Log File](preventing-confidential-information-from-being-written-into-the-log-file.md).</span></span>

## <a name="registry-key"></a><span data-ttu-id="732c2-112">Registrierungsschlüssel</span><span class="sxs-lookup"><span data-stu-id="732c2-112">Registry Key</span></span>

<span data-ttu-id="732c2-113">**HKEY \_ Software Richtlinien für lokale \_ Computer** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="732c2-113">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="732c2-114">Datentyp</span><span class="sxs-lookup"><span data-stu-id="732c2-114">Data Type</span></span>

<span data-ttu-id="732c2-115">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="732c2-115">**REG\_DWORD**</span></span>

 

 
