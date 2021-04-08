---
description: Sie können Richtlinien Module in der Programmiersprache C, C++ oder Visual Basic schreiben.
ms.assetid: 37a93c67-02f2-4c4e-a000-2bb98e0ca948
title: Schreiben von benutzerdefinierten Modulen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92247cd6b975bac520032dcc3aada1328f7b6c2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103959865"
---
# <a name="writing-custom-modules"></a><span data-ttu-id="27f84-103">Schreiben von benutzerdefinierten Modulen</span><span class="sxs-lookup"><span data-stu-id="27f84-103">Writing Custom Modules</span></span>

<span data-ttu-id="27f84-104">Sie können Richtlinien Module in der Programmiersprache C, C++ oder Visual Basic schreiben.</span><span class="sxs-lookup"><span data-stu-id="27f84-104">You can write policy modules in the C, C++, or Visual Basic programming language.</span></span> <span data-ttu-id="27f84-105">Der erforderliche Microsoft-Compiler ist in Visual C++ Version 5,0 oder höher oder in Visual Basic Version 5,0 oder höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="27f84-105">The required Microsoft compiler is available in Visual C++ version 5.0 or later or in Visual Basic version 5.0 or later.</span></span> <span data-ttu-id="27f84-106">Eine Unternehmens [*Zertifizierungsstelle (Certification Authority*](../secgloss/c-gly.md) , ca) sollte nur das von Microsoft bereitgestellte Enterprise Policy-Modul verwenden.</span><span class="sxs-lookup"><span data-stu-id="27f84-106">An enterprise [*certification authority*](../secgloss/c-gly.md) (CA) should use only the Microsoft-provided enterprise policy module.</span></span>

<span data-ttu-id="27f84-107">Sie müssen [**icertpolicy**](/windows/desktop/api/Certpol/nn-certpol-icertpolicy) implementieren, wenn Sie ein benutzerdefiniertes Richtlinien Modul schreiben.</span><span class="sxs-lookup"><span data-stu-id="27f84-107">You must implement [**ICertPolicy**](/windows/desktop/api/Certpol/nn-certpol-icertpolicy) when writing a custom policy module.</span></span> <span data-ttu-id="27f84-108">Außerdem müssen Sie [**icertmanagemodule**](/windows/desktop/api/Certmod/nn-certmod-icertmanagemodule) implementieren, wenn Sie ein benutzerdefiniertes Richtlinien Modul schreiben.</span><span class="sxs-lookup"><span data-stu-id="27f84-108">Additionally, you must implement [**ICertManageModule**](/windows/desktop/api/Certmod/nn-certmod-icertmanagemodule) when writing a custom policy module.</span></span>

<span data-ttu-id="27f84-109">Richtlinien Module können Methoden von [**icertserverpolicy**](/windows/desktop/api/Certif/nn-certif-icertserverpolicy) abrufen, um die Verarbeitung einer [*Zertifikat Anforderung*](../secgloss/c-gly.md)zu unterstützen. **Icertserverpolicy** ermöglicht das Festlegen und Abrufen von Eigenschaften und Zertifikat Erweiterungen.</span><span class="sxs-lookup"><span data-stu-id="27f84-109">Policy modules can call methods from [**ICertServerPolicy**](/windows/desktop/api/Certif/nn-certif-icertserverpolicy) to assist in the processing of a [*certificate request*](../secgloss/c-gly.md); **ICertServerPolicy** allows properties and certificate extensions to be set and retrieved.</span></span>

<span data-ttu-id="27f84-110">Weitere Informationen finden Sie in den nachfolgenden Themen.</span><span class="sxs-lookup"><span data-stu-id="27f84-110">For more information, see the following topics.</span></span>



| <span data-ttu-id="27f84-111">Thema</span><span class="sxs-lookup"><span data-stu-id="27f84-111">Topic</span></span>                                                                      | <span data-ttu-id="27f84-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="27f84-112">Description</span></span>                             |
|----------------------------------------------------------------------------|-----------------------------------------|
| [<span data-ttu-id="27f84-113">Festlegen von Zertifikat Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="27f84-113">Setting Certificate Properties</span></span>](setting-certificate-properties.md)       | <span data-ttu-id="27f84-114">Festlegen der Eigenschaften eines Zertifikats</span><span class="sxs-lookup"><span data-stu-id="27f84-114">Setting the properties of a certificate</span></span> |
| [<span data-ttu-id="27f84-115">Schreiben von benutzerdefinierten Exit-Modulen</span><span class="sxs-lookup"><span data-stu-id="27f84-115">Writing Custom Exit Modules</span></span>](writing-custom-exit-modules.md)             | <span data-ttu-id="27f84-116">Schreiben von benutzerdefinierten Exit-Modulen</span><span class="sxs-lookup"><span data-stu-id="27f84-116">Writing custom exit modules</span></span>             |
| [<span data-ttu-id="27f84-117">Schreiben von benutzerdefinierten Erweiterungs Handlern</span><span class="sxs-lookup"><span data-stu-id="27f84-117">Writing Custom Extension Handlers</span></span>](writing-custom-extension-handlers.md) | <span data-ttu-id="27f84-118">Schreiben von benutzerdefinierten Erweiterungs Handlern</span><span class="sxs-lookup"><span data-stu-id="27f84-118">Writing custom extension handlers</span></span>       |



 

 

 
