---
description: Die WMI-Sicherheitsanbieter können für wmi-Skripts und zum Erstellen eines verwalteten Sicherheitsanbieters verwendet werden.
ms.assetid: c3f7bd91-6cea-43ee-b8a7-1506dbd7926d
title: WMI-Sicherheitsanbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d81833abff5160847678d094694702e4711de90
ms.sourcegitcommit: 822413efb4a70dd464e5db4d9e8693ef74f8132f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2021
ms.locfileid: "113581988"
---
# <a name="security-wmi-providers"></a><span data-ttu-id="3141a-103">WMI-Sicherheitsanbieter</span><span class="sxs-lookup"><span data-stu-id="3141a-103">Security WMI Providers</span></span>

## <a name="purpose"></a><span data-ttu-id="3141a-104">Zweck</span><span class="sxs-lookup"><span data-stu-id="3141a-104">Purpose</span></span>

<span data-ttu-id="3141a-105">Die WMI-Sicherheitsanbieter ermöglichen Es Administratoren und Programmierern, BitLocker-Laufwerkverschlüsselung (BDE) und die Trusted Platform Module (TPM) mithilfe Windows Management Instrumentation (WMI) zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="3141a-105">The Security WMI providers enable administrators and programmers to configure BitLocker Drive Encryption (BDE) and the Trusted Platform Module (TPM) using Windows Management Instrumentation (WMI).</span></span>

## <a name="developer-audience"></a><span data-ttu-id="3141a-106">Entwicklergruppe</span><span class="sxs-lookup"><span data-stu-id="3141a-106">Developer audience</span></span>

<span data-ttu-id="3141a-107">Dieses Dokument gibt die WMI-Anbieterschnittstelle zum Verwalten und Konfigurieren von BitLocker-Laufwerkverschlüsselung (BDE) und Trusted Platform Module (TPM) auf Windows Server 2008 R2 und Windows Server 2008 für Server sowie Windows 7 und Windows Vista für Clientcomputer an.</span><span class="sxs-lookup"><span data-stu-id="3141a-107">This document specifies the WMI provider interface for managing and configuring BitLocker Drive Encryption (BDE) and Trusted Platform Module (TPM) on Windows Server 2008 R2 and Windows Server 2008 for servers, and Windows 7 and Windows Vista for client computers.</span></span> <span data-ttu-id="3141a-108">Sie soll von Benutzern gelesen werden, die Skripts, Benutzeroberflächenelemente oder andere Verwaltungstools für BDE oder tpm schreiben.</span><span class="sxs-lookup"><span data-stu-id="3141a-108">It is intended to be read by those writing scripts, user interface elements, or other administrative tools for BDE or the TPM.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="3141a-109">Laufzeitanforderungen</span><span class="sxs-lookup"><span data-stu-id="3141a-109">Run-time requirements</span></span>

<span data-ttu-id="3141a-110">Die WMI-Sicherheitsanbieter erfordern die MOF-Datei, die mit jedem Anbieter und einem unterstützten Betriebssystem angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="3141a-110">The Security WMI Providers require the .mof file specified with each provider and a supported operating system.</span></span> <span data-ttu-id="3141a-111">Das Mindestbetriebssystem ist entweder Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="3141a-111">The minimum operating system is either Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="3141a-112">BitLocker-Laufwerkverschlüsselung ist nur für die versionen Windows Vista Enterprise und Windows Vista Ultimate von Windows Vista verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3141a-112">BitLocker Drive Encryption is only available for the Windows Vista Enterprise and Windows Vista Ultimate versions of Windows Vista.</span></span> <span data-ttu-id="3141a-113">Informationen zu Laufzeitanforderungen für ein bestimmtes Programmierelement finden Sie im Abschnitt Anforderungen der Referenzseite für dieses Element.</span><span class="sxs-lookup"><span data-stu-id="3141a-113">For information about run-time requirements for a particular programming element, see the Requirements section of the reference page for that element.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="3141a-114">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="3141a-114">In this section</span></span>



| <span data-ttu-id="3141a-115">Thema</span><span class="sxs-lookup"><span data-stu-id="3141a-115">Topic</span></span>                                                                               | <span data-ttu-id="3141a-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3141a-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="3141a-117">Informationen zu WMI-Sicherheitsanbietern</span><span class="sxs-lookup"><span data-stu-id="3141a-117">About Security WMI Providers</span></span>](about-security-wmi-providers.md)<br/>         | <span data-ttu-id="3141a-118">Kurze Übersicht über die Sicherheits-WMI-Anbieter.</span><span class="sxs-lookup"><span data-stu-id="3141a-118">Brief overview of the Security WMI Providers.</span></span><br/>           |
| [<span data-ttu-id="3141a-119">WMI-Anbieterreferenz für die Sicherheit</span><span class="sxs-lookup"><span data-stu-id="3141a-119">Security WMI Providers Reference</span></span>](security-wmi-providers-reference.md)<br/> | <span data-ttu-id="3141a-120">Referenzdokumentation für die Sicherheits-WMI-Anbieter.</span><span class="sxs-lookup"><span data-stu-id="3141a-120">Reference documentation for the Security WMI Providers.</span></span><br/> |



 

## <a name="additional-resources"></a><span data-ttu-id="3141a-121">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="3141a-121">Additional resources</span></span>

<span data-ttu-id="3141a-122">Im Folgenden finden Sie zusätzliche Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="3141a-122">The following are additional resources.</span></span>



| <span data-ttu-id="3141a-123">Resource</span><span class="sxs-lookup"><span data-stu-id="3141a-123">Resource</span></span>     | <span data-ttu-id="3141a-124">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3141a-124">Description</span></span>                                                                                                                                               |
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3141a-125">Klassen</span><span class="sxs-lookup"><span data-stu-id="3141a-125">Classes</span></span>      | <span data-ttu-id="3141a-126">Weitere Informationen zu den WMI-Sicherheitsanbietern finden Sie unter [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) und [**Win32 \_ Tpm**](win32-tpm.md).</span><span class="sxs-lookup"><span data-stu-id="3141a-126">For more information about the Security WMI providers, see [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) and [**Win32\_Tpm**](win32-tpm.md).</span></span> |



 

 

 




