---
description: Das System lädt einen Zeit Anbieter basierend auf seinen Konfigurationsinformationen, die in der Registrierung gespeichert sind.
ms.assetid: 67f79c31-9dd7-4e3f-bfe1-701b10611f91
title: Registrieren eines Zeit Anbieters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a98e5e516db6b2c800c917c5e47da9bd75ba5c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865707"
---
# <a name="registering-a-time-provider"></a><span data-ttu-id="7eaf0-103">Registrieren eines Zeit Anbieters</span><span class="sxs-lookup"><span data-stu-id="7eaf0-103">Registering a Time Provider</span></span>

<span data-ttu-id="7eaf0-104">Das System lädt einen Zeit Anbieter basierend auf seinen Konfigurationsinformationen, die in der Registrierung gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="7eaf0-104">The system loads a time provider based on its configuration information stored in the registry.</span></span> <span data-ttu-id="7eaf0-105">Jedes Mal, wenn der Anbieter den folgenden Registrierungsschlüssel erstellen sollte:</span><span class="sxs-lookup"><span data-stu-id="7eaf0-105">Each time provider should create the following registry key:</span></span>

<span data-ttu-id="7eaf0-106">**HKEY \_ Lokales \_ Computer \\ System** \\ **CurrentControlSet** \\ **Services** \\ **W32Time** \\ **Zeit Anbieter** \\ *providerName*</span><span class="sxs-lookup"><span data-stu-id="7eaf0-106">**HKEY\_LOCAL\_MACHINE\\System**\\**CurrentControlSet**\\**Services**\\**W32Time**\\**TimeProviders**\\*ProviderName*</span></span>

<span data-ttu-id="7eaf0-107">In der folgenden Tabelle werden die Werte beschrieben, die im Schlüssel jedes Anbieters vorhanden sein müssen.</span><span class="sxs-lookup"><span data-stu-id="7eaf0-107">The following table describes the values that must exist in each provider's key.</span></span>



| <span data-ttu-id="7eaf0-108">Wert</span><span class="sxs-lookup"><span data-stu-id="7eaf0-108">Value</span></span>             | <span data-ttu-id="7eaf0-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7eaf0-109">Description</span></span>                                                                                                                                                                                                              |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7eaf0-110">**DllName**</span><span class="sxs-lookup"><span data-stu-id="7eaf0-110">**DllName**</span></span>       | <span data-ttu-id="7eaf0-111">Der Name der dll, die den Anbieter enthält.</span><span class="sxs-lookup"><span data-stu-id="7eaf0-111">The name of the DLL that contains the provider.</span></span> <span data-ttu-id="7eaf0-112">Dieser Wert weist den Typ **reg \_ SZ** auf.</span><span class="sxs-lookup"><span data-stu-id="7eaf0-112">This value has the type **REG\_SZ**.</span></span>                                                                                                                                     |
| <span data-ttu-id="7eaf0-113">**Aktiviert**</span><span class="sxs-lookup"><span data-stu-id="7eaf0-113">**Enabled**</span></span>       | <span data-ttu-id="7eaf0-114">Gibt an, ob der Anbieter gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7eaf0-114">Indicates whether the provider should be started.</span></span> <span data-ttu-id="7eaf0-115">Wenn dieser Wert 1 ist, wird der Anbieter gestartet.</span><span class="sxs-lookup"><span data-stu-id="7eaf0-115">If this value is 1, the provider is started.</span></span> <span data-ttu-id="7eaf0-116">Andernfalls wird der Anbieter nicht gestartet.</span><span class="sxs-lookup"><span data-stu-id="7eaf0-116">Otherwise, the provider is not started.</span></span> <span data-ttu-id="7eaf0-117">Dieser Wert weist den Typ " **reg \_ DWORD**" auf.</span><span class="sxs-lookup"><span data-stu-id="7eaf0-117">This value has the type **REG\_DWORD**.</span></span>                                           |
| <span data-ttu-id="7eaf0-118">**InputProvider**</span><span class="sxs-lookup"><span data-stu-id="7eaf0-118">**InputProvider**</span></span> | <span data-ttu-id="7eaf0-119">Gibt an, ob der Anbieter ein Eingabe-oder Ausgabe Anbieter ist.</span><span class="sxs-lookup"><span data-stu-id="7eaf0-119">Indicates whether the provider is an input provider or an output provider.</span></span> <span data-ttu-id="7eaf0-120">Wenn dieser Wert 1 ist, ist der Anbieter ein Eingabe Anbieter.</span><span class="sxs-lookup"><span data-stu-id="7eaf0-120">If this value is 1, the provider is an input provider.</span></span> <span data-ttu-id="7eaf0-121">Andernfalls ist der Anbieter ein Ausgabe Anbieter.</span><span class="sxs-lookup"><span data-stu-id="7eaf0-121">Otherwise, the provider is an output provider.</span></span> <span data-ttu-id="7eaf0-122">Dieser Wert weist den Typ " **reg \_ DWORD**" auf.</span><span class="sxs-lookup"><span data-stu-id="7eaf0-122">This value has the type **REG\_DWORD**.</span></span> |



 

<span data-ttu-id="7eaf0-123">Der Zeit Anbieter-Manager listet die Schlüssel unter dem Schlüssel **timeproviders** auf und startet jeden aktivierten Anbieter.</span><span class="sxs-lookup"><span data-stu-id="7eaf0-123">The time provider manager enumerates the keys under the **TimeProviders** key and starts each enabled provider.</span></span> <span data-ttu-id="7eaf0-124">Anbieter werden beim Systemstart gestartet und immer dann, wenn Parameter geändert werden.</span><span class="sxs-lookup"><span data-stu-id="7eaf0-124">Providers are started at system startup and whenever there are parameter changes.</span></span>

<span data-ttu-id="7eaf0-125">Jeder Anbieter kann auch anwendungsspezifische Konfigurationsinformationen in der Registrierung speichern.</span><span class="sxs-lookup"><span data-stu-id="7eaf0-125">Each time provider can also store application-specific configuration information in the registry.</span></span>

 

 



