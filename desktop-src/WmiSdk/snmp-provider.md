---
description: Der SNMP-Anbieter (Simple Network Management Protocol) ermöglicht Client Anwendungen den Zugriff auf SNMP-Informationen über Windows-Verwaltungsinstrumentation (WMI).
ms.assetid: 71e758d9-2ea6-42f5-93b4-d370a96b10cf
ms.tgt_platform: multiple
title: WMI und SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5ea7e8385e1fb95ac20d14af31f82444350e044
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218489"
---
# <a name="wmi-and-snmp"></a><span data-ttu-id="4b6f7-103">WMI und SNMP</span><span class="sxs-lookup"><span data-stu-id="4b6f7-103">WMI and SNMP</span></span>

<span data-ttu-id="4b6f7-104">Der SNMP-Anbieter (Simple Network Management Protocol) ermöglicht Client Anwendungen den Zugriff auf SNMP-Informationen über Windows-Verwaltungsinstrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="4b6f7-104">The Simple Network Management Protocol (SNMP) provider allows client applications to access SNMP information through Windows Management Instrumentation (WMI).</span></span> <span data-ttu-id="4b6f7-105">Der SNMP-Anbieter ist standardmäßig nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="4b6f7-105">The SNMP provider is not installed by default.</span></span> <span data-ttu-id="4b6f7-106">Weitere Informationen zum Installieren des Anbieters finden Sie unter [Einrichten der WMI-SNMP-Umgebung](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="4b6f7-106">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

<span data-ttu-id="4b6f7-107">SNMP (Simple Network Management Protocol) verwendet ein Schema zum Definieren von Objekten.</span><span class="sxs-lookup"><span data-stu-id="4b6f7-107">Simple Network Management Protocol (SNMP) uses a schema to define objects.</span></span> <span data-ttu-id="4b6f7-108">Das Schema unterscheidet sich von dem in WMI verwendeten Schema.</span><span class="sxs-lookup"><span data-stu-id="4b6f7-108">The schema is different from the schema used in WMI.</span></span> <span data-ttu-id="4b6f7-109">Das Schema SNMPv1 und SNMPv2C wird als Struktur von Verwaltungsinformationen (SMI) bezeichnet und als MIB-Dateien (Management Information Base) verpackt.</span><span class="sxs-lookup"><span data-stu-id="4b6f7-109">The SNMPv1 and SNMPv2C schema is called the Structure of Management Information (SMI), and is packaged as Management Information Base (MIB) files.</span></span> <span data-ttu-id="4b6f7-110">MIB-Dateien definieren Objekte mithilfe einer Standardsprache – Abstract Syntax Notation 1 (ASN. 1) – und einer Reihe von Makro Definitionen, die als Vorlagen zum Beschreiben der Objekte dienen.</span><span class="sxs-lookup"><span data-stu-id="4b6f7-110">MIB files define objects using a standard language—Abstract Syntax Notation 1 (ASN.1)—and a number of macro definitions that serve as templates for describing the objects.</span></span> <span data-ttu-id="4b6f7-111">Die Makros stellen Informationen wie den Objektnamen, den Bezeichner, die Syntax, die Beschreibung, Zugriffsrechte, Protokoll Vorgänge und die Protokoll Codierung bereit.</span><span class="sxs-lookup"><span data-stu-id="4b6f7-111">The macros provide information such as the object name, identifier, syntax, description, access rights, protocol operations, and protocol encoding.</span></span> <span data-ttu-id="4b6f7-112">In der folgenden Tabelle ist aufgelistet, wie der SNMP-Anbieter verschiedene Aspekte eines MIB-Objekts behandelt.</span><span class="sxs-lookup"><span data-stu-id="4b6f7-112">The following table lists how the SNMP provider handles different aspects of a MIB object.</span></span>



| <span data-ttu-id="4b6f7-113">Thema</span><span class="sxs-lookup"><span data-stu-id="4b6f7-113">Topic</span></span>                                                    | <span data-ttu-id="4b6f7-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4b6f7-114">Description</span></span>                                                 |
|----------------------------------------------------------|-------------------------------------------------------------|
| [<span data-ttu-id="4b6f7-115">Notification-Type-Makro</span><span class="sxs-lookup"><span data-stu-id="4b6f7-115">NOTIFICATION-TYPE Macro</span></span>](notification-type-macro.md)   | <span data-ttu-id="4b6f7-116">Gibt an, wie das **-Benachrichtigungstyp-** Makro von SNMP zu WMI zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="4b6f7-116">How the **NOTIFICATION-TYPE** macro maps from SNMP to WMI.</span></span>  |
| [<span data-ttu-id="4b6f7-117">Object-Type-Makro</span><span class="sxs-lookup"><span data-stu-id="4b6f7-117">OBJECT-TYPE Macro</span></span>](object-type-macro.md)               | <span data-ttu-id="4b6f7-118">Gibt an, wie das **Objekttyp-** Makro von SNMP zu WMI zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="4b6f7-118">How the **OBJECT-TYPE** macro maps from SNMP to WMI.</span></span>        |
| [<span data-ttu-id="4b6f7-119">Text Konvention-Makro</span><span class="sxs-lookup"><span data-stu-id="4b6f7-119">TEXTUAL-CONVENTION Macro</span></span>](textual-convention-macro.md) | <span data-ttu-id="4b6f7-120">Gibt an, wie das **Textkonventionen-** Makro von SNMP zu WMI zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="4b6f7-120">How the **TEXTUAL-CONVENTION** macro maps from SNMP to WMI.</span></span> |
| [<span data-ttu-id="4b6f7-121">Trap-Type-Makro</span><span class="sxs-lookup"><span data-stu-id="4b6f7-121">TRAP-TYPE Macro</span></span>](trap-type-macro.md)                   | <span data-ttu-id="4b6f7-122">Gibt an, wie das **Trap-Type-** Makro von SNMP zu WMI zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="4b6f7-122">How the **TRAP-TYPE** macro maps from SNMP to WMI.</span></span>          |



 

<span data-ttu-id="4b6f7-123">Der SNMP-Anbieter enthält einen Compiler, der MIB-Objekte in WMI-Objekte übersetzt.</span><span class="sxs-lookup"><span data-stu-id="4b6f7-123">The SNMP provider comes with a compiler that translates MIB objects into WMI objects.</span></span> <span data-ttu-id="4b6f7-124">Der SNMP-Compiler kann auch Fehler oder andere Nachrichten ausgeben.</span><span class="sxs-lookup"><span data-stu-id="4b6f7-124">The SNMP compiler can also output error or other messages.</span></span> <span data-ttu-id="4b6f7-125">Weitere Informationen finden Sie unter [SNMP-Compilerfehlermeldungen](snmp-compiler-error-messages.md) und [Allgemeine Informationsmeldungen](general-information-messages.md).</span><span class="sxs-lookup"><span data-stu-id="4b6f7-125">For more information, see [SNMP compiler Error Messages](snmp-compiler-error-messages.md) and [General Information Messages](general-information-messages.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4b6f7-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4b6f7-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4b6f7-127">WMI-Referenz</span><span class="sxs-lookup"><span data-stu-id="4b6f7-127">WMI Reference</span></span>](wmi-reference.md)
</dt> <dt>

[<span data-ttu-id="4b6f7-128">WMI-Anbieter</span><span class="sxs-lookup"><span data-stu-id="4b6f7-128">WMI Providers</span></span>](wmi-providers.md)
</dt> </dl>

 

 



