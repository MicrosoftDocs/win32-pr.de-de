---
description: Die Debugversion der XAudio2-Engine überprüft Parameter und stellt ausführliche Warn-und Fehlermeldungen bereit.
ms.assetid: a7aaebf9-98d4-e96c-993d-b0d0b7074788
title: XAudio2-Debugging-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc50e710f30969e024078eeaf2660545e1da45c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752409"
---
# <a name="xaudio2-debugging-facilities"></a><span data-ttu-id="8c196-103">XAudio2-Debugging-Funktionen</span><span class="sxs-lookup"><span data-stu-id="8c196-103">XAudio2 Debugging Facilities</span></span>

<span data-ttu-id="8c196-104">Die Debugversion der XAudio2-Engine überprüft Parameter und stellt ausführliche Warn-und Fehlermeldungen bereit.</span><span class="sxs-lookup"><span data-stu-id="8c196-104">The debug version of the XAudio2 engine validates parameters, and provides detailed warning and error messages.</span></span>

## <a name="setting-the-debug-logging-level-at-run-time"></a><span data-ttu-id="8c196-105">Festlegen der debugprotokollierungs Stufe zur Laufzeit</span><span class="sxs-lookup"><span data-stu-id="8c196-105">Setting the Debug Logging Level at Run Time</span></span>

<span data-ttu-id="8c196-106">Sie können die Ebene der Debuginformationen, die von XAudio2 angezeigt werden, jederzeit festlegen, indem Sie eine [**XAudio2 \_ Debug- \_ Konfigurations**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_debug_configuration) Struktur mit den Flags für den gewünschten Protokolliergrad ausfüllen und die Struktur dann an die [**IXAudio2:: setdebugconfiguration**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-setdebugconfiguration) -Methode übergeben.</span><span class="sxs-lookup"><span data-stu-id="8c196-106">You can set the level of debugging information shown by XAudio2 at any time by filling out an [**XAUDIO2\_DEBUG\_CONFIGURATION**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_debug_configuration) structure with the flags for the desired logging level, and then pass the structure to the [**IXAudio2::SetDebugConfiguration**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-setdebugconfiguration) method.</span></span> <span data-ttu-id="8c196-107">Werte, die an die **IXAudio2:: setdebugconfiguration** -Methode übergeben werden, überschreiben immer alle Standardwerte, die in der Windows-Registrierung festgelegt wurden.</span><span class="sxs-lookup"><span data-stu-id="8c196-107">Values passed to the **IXAudio2::SetDebugConfiguration** method always override any default values that were set in the Windows registry.</span></span>

## <a name="debug-support"></a><span data-ttu-id="8c196-108">Debugunterstützung</span><span class="sxs-lookup"><span data-stu-id="8c196-108">Debug Support</span></span>

<span data-ttu-id="8c196-109">Die Debuggingfunktionen sind für XAUDIO2 in Windows 8 immer verfügbar.</span><span class="sxs-lookup"><span data-stu-id="8c196-109">The debugging facilities are always available for XAUDIO2 in Windows 8.</span></span>

<span data-ttu-id="8c196-110">Für die DirectX SDK-Versionen von XAUDIO2 müssen Sie die **XAUDIO2 \_ Debug- \_ Engine** verwenden, wenn Sie das XAUDIO2-Objekt mit [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) erstellen, und das System muss die DirectX SDK Developer Runtime installiert haben, damit das Debugging unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="8c196-110">For the DirectX SDK versions of XAUDIO2, you must use **XAUDIO2\_DEBUG\_ENGINE** when creating the XAUDIO2 object with [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) and the system must have the DirectX SDK Developer Runtime installed for debugging to be supported.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8c196-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8c196-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c196-112">Debugging-Einrichtungen</span><span class="sxs-lookup"><span data-stu-id="8c196-112">Debugging Facilities</span></span>](debugging-facilities.md)
</dt> <dt>

[<span data-ttu-id="8c196-113">XAudio2-Programmierreferenz</span><span class="sxs-lookup"><span data-stu-id="8c196-113">XAudio2 Programming Reference</span></span>](programming-reference.md)
</dt> </dl>

 

 
