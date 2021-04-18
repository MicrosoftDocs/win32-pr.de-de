---
description: Die WMI-Sicherheitsanbieter können für die WMI-Skripterstellung und für die Erstellung eines verwalteten Sicherheits Anbieters verwendet werden.
ms.assetid: c3f7bd91-6cea-43ee-b8a7-1506dbd7926d
title: WMI-Anbieter für Sicherheit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0206e337e5fa23470f015a0264bd77d53e8c4e14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354449"
---
# <a name="security-wmi-providers"></a><span data-ttu-id="9afc8-103">WMI-Anbieter für Sicherheit</span><span class="sxs-lookup"><span data-stu-id="9afc8-103">Security WMI Providers</span></span>

## <a name="purpose"></a><span data-ttu-id="9afc8-104">Zweck</span><span class="sxs-lookup"><span data-stu-id="9afc8-104">Purpose</span></span>

<span data-ttu-id="9afc8-105">Die WMI-Anbieter für Sicherheit ermöglichen es Administratoren und Programmierern, BitLocker-Laufwerkverschlüsselung (BDE) und Trusted Platform Module (TPM) mithilfe von Windows-Verwaltungsinstrumentation (WMI) zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="9afc8-105">The Security WMI providers enable administrators and programmers to configure BitLocker Drive Encryption (BDE) and the Trusted Platform Module (TPM) using Windows Management Instrumentation (WMI).</span></span>

## <a name="developer-audience"></a><span data-ttu-id="9afc8-106">Entwicklergruppe</span><span class="sxs-lookup"><span data-stu-id="9afc8-106">Developer audience</span></span>

<span data-ttu-id="9afc8-107">In diesem Dokument wird die WMI-Anbieter Schnittstelle zum Verwalten und Konfigurieren von BitLocker-Laufwerkverschlüsselung (BDE) und Trusted Platform Module (TPM) auf Windows Server 2008 R2 und Windows Server 2008 für-Server sowie Windows 7 und Windows Vista für Client Computer angegeben.</span><span class="sxs-lookup"><span data-stu-id="9afc8-107">This document specifies the WMI provider interface for managing and configuring BitLocker Drive Encryption (BDE) and Trusted Platform Module (TPM) on Windows Server 2008 R2 and Windows Server 2008 for servers, and Windows 7 and Windows Vista for client computers.</span></span> <span data-ttu-id="9afc8-108">Sie soll von denjenigen gelesen werden, die Skripts, Benutzeroberflächen Elemente oder andere Verwaltungs Tools für BDE oder das TPM schreiben.</span><span class="sxs-lookup"><span data-stu-id="9afc8-108">It is intended to be read by those writing scripts, user interface elements, or other administrative tools for BDE or the TPM.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="9afc8-109">Laufzeitanforderungen</span><span class="sxs-lookup"><span data-stu-id="9afc8-109">Run-time requirements</span></span>

<span data-ttu-id="9afc8-110">Die WMI-Sicherheitsanbieter benötigen die MOF-Datei, die mit den einzelnen Anbietern und einem unterstützten Betriebssystem angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="9afc8-110">The Security WMI Providers require the .mof file specified with each provider and a supported operating system.</span></span> <span data-ttu-id="9afc8-111">Das mindestbetriebssystem ist entweder Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9afc8-111">The minimum operating system is either Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="9afc8-112">BitLocker-Laufwerkverschlüsselung ist nur für die Windows Vista Enterprise-und Windows Vista Ultimate-Versionen von Windows Vista verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9afc8-112">BitLocker Drive Encryption is only available for the Windows Vista Enterprise and Windows Vista Ultimate versions of Windows Vista.</span></span> <span data-ttu-id="9afc8-113">Informationen zu den Lauf Zeitanforderungen für ein bestimmtes Programmier Element finden Sie im Abschnitt "Anforderungen" der Referenzseite für dieses Element.</span><span class="sxs-lookup"><span data-stu-id="9afc8-113">For information about run-time requirements for a particular programming element, see the Requirements section of the reference page for that element.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="9afc8-114">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="9afc8-114">In this section</span></span>



| <span data-ttu-id="9afc8-115">Thema</span><span class="sxs-lookup"><span data-stu-id="9afc8-115">Topic</span></span>                                                                               | <span data-ttu-id="9afc8-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9afc8-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="9afc8-117">Informationen zu WMI-Sicherheitsanbietern</span><span class="sxs-lookup"><span data-stu-id="9afc8-117">About Security WMI Providers</span></span>](about-security-wmi-providers.md)<br/>         | <span data-ttu-id="9afc8-118">Kurze Übersicht über die WMI-Sicherheitsanbieter.</span><span class="sxs-lookup"><span data-stu-id="9afc8-118">Brief overview of the Security WMI Providers.</span></span><br/>           |
| [<span data-ttu-id="9afc8-119">WMI-Anbieter Referenz für Sicherheit</span><span class="sxs-lookup"><span data-stu-id="9afc8-119">Security WMI Providers Reference</span></span>](security-wmi-providers-reference.md)<br/> | <span data-ttu-id="9afc8-120">Referenz Dokumentation für die WMI-Sicherheitsanbieter.</span><span class="sxs-lookup"><span data-stu-id="9afc8-120">Reference documentation for the Security WMI Providers.</span></span><br/> |



 

## <a name="additional-resources"></a><span data-ttu-id="9afc8-121">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="9afc8-121">Additional resources</span></span>

<span data-ttu-id="9afc8-122">Im folgenden finden Sie weitere Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="9afc8-122">The following are additional resources.</span></span>



|                    |                                                                                                                                                                        |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9afc8-123">Klassen</span><span class="sxs-lookup"><span data-stu-id="9afc8-123">Classes</span></span><br/> | <span data-ttu-id="9afc8-124">Weitere Informationen zu den WMI-Sicherheitsanbietern finden Sie unter [**Win32 \_ verschlüsseltablevolume**](win32-encryptablevolume.md) und [**Win32 \_ TPM**](win32-tpm.md).</span><span class="sxs-lookup"><span data-stu-id="9afc8-124">For more information about the Security WMI providers, see [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) and [**Win32\_Tpm**](win32-tpm.md).</span></span><br/> |



 

 

 




