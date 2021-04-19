---
description: Wenn diese pro-Computer-System Richtlinie auf &\# 0034; 1&0034; festgelegt ist \# , verhindert das Installationsprogramm, dass nicht Administratoren die Benutzerkontensteuerung (User Account Control, UAC) für alle auf dem Computer installierten Anwendungen verwenden.
ms.assetid: b122d6f4-2be6-4b9b-b8e0-ca08fe9c4f94
title: Disableluapatching
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b76357211523d0a69a56ab2a047623a63f211df9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106355079"
---
# <a name="disableluapatching"></a><span data-ttu-id="32be8-103">Disableluapatching</span><span class="sxs-lookup"><span data-stu-id="32be8-103">DisableLUAPatching</span></span>

<span data-ttu-id="32be8-104">Wenn diese pro-Computer-System Richtlinie auf "1" festgelegt ist, verhindert das Installationsprogramm, dass nicht Administratoren die [Benutzerkontensteuerung (User Account Control, UAC)](user-account-control--uac--patching.md) für alle auf dem Computer installierten Anwendungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="32be8-104">If this per-machine system policy is set to "1", the installer prevents non-administrators from using [User Account Control (UAC) Patching](user-account-control--uac--patching.md) for any application installed on the computer.</span></span> <span data-ttu-id="32be8-105">Wenn die System Richtlinie pro Computer nicht festgelegt oder auf 0 festgelegt ist, können nicht Administratoren benutzerpatches mit geringsten Rechten auf Anwendungen anwenden, die für das Patchen von Benutzerkonten mit geringsten Rechten aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="32be8-105">When the per-machine system policy is not set or set to 0, non-administrators can apply least-privilege user patches to applications that are enabled for least-privilege user account patching.</span></span>

<span data-ttu-id="32be8-106">Verwenden Sie die [**msidisableluapatching**](msidisableluapatching.md) -Eigenschaft, um das Patchen einer Anwendung mit den geringsten Berechtigungen zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="32be8-106">Use the [**MSIDISABLELUAPATCHING**](msidisableluapatching.md) property to prevent the least-privilege patching of an application.</span></span>

<span data-ttu-id="32be8-107">Die Richtlinie "disableluapatching" ist ab Windows Installer Version 3,0 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="32be8-107">The DisableLUAPatching policy is available beginning with Windows Installer version 3.0.</span></span>

## <a name="registry-key"></a><span data-ttu-id="32be8-108">Registrierungsschlüssel</span><span class="sxs-lookup"><span data-stu-id="32be8-108">Registry Key</span></span>

<span data-ttu-id="32be8-109">**HKEY \_ Software Richtlinien für lokale \_ Computer** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="32be8-109">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="32be8-110">Datentyp</span><span class="sxs-lookup"><span data-stu-id="32be8-110">Data Type</span></span>

<span data-ttu-id="32be8-111">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="32be8-111">**REG\_DWORD**</span></span>

## <a name="related-topics"></a><span data-ttu-id="32be8-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="32be8-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="32be8-113">Wird in Windows Installer 2,0 und früher nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="32be8-113">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



