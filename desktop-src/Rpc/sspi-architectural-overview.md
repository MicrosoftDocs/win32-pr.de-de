---
title: Übersicht über die SSPI-Architektur
description: SSPI ist eine Softwareschnittstelle.
ms.assetid: 2497afea-33dd-45ae-891b-bacf390ef338
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 910cef52def2f398606fd541b8ed170f7e216078
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039336"
---
# <a name="sspi-architectural-overview"></a><span data-ttu-id="f2dfb-103">Übersicht über die SSPI-Architektur</span><span class="sxs-lookup"><span data-stu-id="f2dfb-103">SSPI Architectural Overview</span></span>

<span data-ttu-id="f2dfb-104">SSPI ist eine Softwareschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="f2dfb-104">SSPI is a software interface.</span></span> <span data-ttu-id="f2dfb-105">Verteilte Programmierbibliotheken, z. b. RPC, können diese für authentifizierte Kommunikation verwenden.</span><span class="sxs-lookup"><span data-stu-id="f2dfb-105">Distributed programming libraries such as RPC can use it for authenticated communications.</span></span> <span data-ttu-id="f2dfb-106">Ein oder mehrere Softwaremodule bieten die eigentlichen Authentifizierungsfunktionen.</span><span class="sxs-lookup"><span data-stu-id="f2dfb-106">One or more software modules provide the actual authentication capabilities.</span></span> <span data-ttu-id="f2dfb-107">Jedes Modul, das als Security Support Provider (SSP) bezeichnet wird, wird als Dynamic Link Library (dll) implementiert.</span><span class="sxs-lookup"><span data-stu-id="f2dfb-107">Each module, called a security support provider (SSP), is implemented as a dynamic link library (DLL).</span></span> <span data-ttu-id="f2dfb-108">Ein SSP stellt mindestens ein Sicherheitspaket bereit.</span><span class="sxs-lookup"><span data-stu-id="f2dfb-108">An SSP provides one or more security packages.</span></span>

<span data-ttu-id="f2dfb-109">Es stehen eine Vielzahl von SSPs und Paketen zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="f2dfb-109">A variety of SSPs and packages are available.</span></span> <span data-ttu-id="f2dfb-110">Windows umfasst das NTLM-Sicherheitspaket und das Microsoft Kerberos-Protokoll Sicherheitspaket.</span><span class="sxs-lookup"><span data-stu-id="f2dfb-110">Windows ships with the NTLM security package and the Microsoft Kerberos protocol security package.</span></span> <span data-ttu-id="f2dfb-111">Außerdem können Sie das Sicherheitspaket Secure Socket Layer (SSL) oder einen beliebigen anderen SSPI-kompatiblen SSP installieren.</span><span class="sxs-lookup"><span data-stu-id="f2dfb-111">In addition, you may choose to install the Secure Socket Layer (SSL) security package, or any other SSPI-compatible SSP.</span></span>

<span data-ttu-id="f2dfb-112">Durch die Verwendung von SSPI wird sichergestellt, dass die Anwendung unabhängig davon, welche SSP Sie auswählen, auf einheitliche Weise auf die Authentifizierungs Features zugreift.</span><span class="sxs-lookup"><span data-stu-id="f2dfb-112">Using SSPI ensures that no matter which SSP you select, your application accesses the authentication features in a uniform manner.</span></span> <span data-ttu-id="f2dfb-113">Diese Funktion bietet Ihrer Anwendung mehr Unabhängigkeit als die Implementierung des Netzwerks, als in der Vergangenheit verfügbar war.</span><span class="sxs-lookup"><span data-stu-id="f2dfb-113">This capability provides your application greater independence from the implementation of the network than was available in the past.</span></span>

<span data-ttu-id="f2dfb-114">Verteilte Anwendungen kommunizieren über die RPC-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="f2dfb-114">Distributed applications communicate through the RPC interface.</span></span> <span data-ttu-id="f2dfb-115">Die RPC-Software greift wiederum über die SSPI auf die Authentifizierungs Features eines SSP zu.</span><span class="sxs-lookup"><span data-stu-id="f2dfb-115">The RPC software in turn, accesses the authentication features of an SSP through the SSPI.</span></span>

<span data-ttu-id="f2dfb-116">Weitere Informationen finden Sie unter [SSPI](/windows/desktop/SecAuthN/sspi).</span><span class="sxs-lookup"><span data-stu-id="f2dfb-116">For more information, see [SSPI](/windows/desktop/SecAuthN/sspi).</span></span>

 

 