---
description: Manchmal müssen Sie möglicherweise eine neuere Version eines Anbieters auf einem laufenden System installieren.
ms.assetid: 44c4c16a-fd79-483a-81ef-a0f74a2cdf45
ms.tgt_platform: multiple
title: Aktualisieren eines Anbieters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4869e6e9f7fbddc3081922f476ca021934065a18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349983"
---
# <a name="updating-a-provider"></a><span data-ttu-id="51e70-103">Aktualisieren eines Anbieters</span><span class="sxs-lookup"><span data-stu-id="51e70-103">Updating a Provider</span></span>

<span data-ttu-id="51e70-104">Manchmal müssen Sie möglicherweise eine neuere Version eines Anbieters auf einem laufenden System installieren.</span><span class="sxs-lookup"><span data-stu-id="51e70-104">Sometimes you may need to install a newer version of a provider onto a running system.</span></span> <span data-ttu-id="51e70-105">Wenn Ihr Anbieter als DLL installiert ist, können Sie einen neuen Anbieter installieren, ohne den Dienst neu starten zu müssen, den Computer neu starten oder andere Anwendungen, die WMI verwenden, zu diesem Zeitpunkt anderweitig beeinflussen können.</span><span class="sxs-lookup"><span data-stu-id="51e70-105">If your provider is installed as a DLL, you can install a new provider without having to restart the service, reboot the computer, or otherwise affect any applications using WMI at that time.</span></span>

<span data-ttu-id="51e70-106">Im folgenden Verfahren wird beschrieben, wie ein-Anbieter aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="51e70-106">The following procedure describes how to update a provider.</span></span>

<span data-ttu-id="51e70-107">**So aktualisieren Sie einen Anbieter**</span><span class="sxs-lookup"><span data-stu-id="51e70-107">**To update a provider**</span></span>

1.  <span data-ttu-id="51e70-108">Erstellen Sie den neuen Anbieter.</span><span class="sxs-lookup"><span data-stu-id="51e70-108">Build the new provider.</span></span>

    1.  <span data-ttu-id="51e70-109">Kompilieren Sie den neuen Anbieter mit einem anderen DLL-Namen und einer anderen **CLSID**.</span><span class="sxs-lookup"><span data-stu-id="51e70-109">Compile the new provider with a different DLL name and a different **CLSID**.</span></span>

        <span data-ttu-id="51e70-110">Ändern Sie beispielsweise Myprov.dll in Myprov1.dll und **CLSID \_ myproprov** in **CLSID \_ MyProv** 1.</span><span class="sxs-lookup"><span data-stu-id="51e70-110">For example, change Myprov.dll to Myprov1.dll, and **CLSID\_MyProProv** to **CLSID\_MyProv** 1.</span></span>

    2.  <span data-ttu-id="51e70-111">Ändern Sie die MOF-Datei für die Anbieter Registrierung so, dass Sie die neue CLSID (CLSID \_ MyProv1), jedoch den gleichen Anbieter Namen ("MyProv") verwendet.</span><span class="sxs-lookup"><span data-stu-id="51e70-111">Modify the provider registration MOF file to use the new CLSID (CLSID\_MyProv1), but the same provider name ("MyProv").</span></span>

2.  <span data-ttu-id="51e70-112">Installieren Sie den neuen Anbieter.</span><span class="sxs-lookup"><span data-stu-id="51e70-112">Install the new provider.</span></span>

    1.  <span data-ttu-id="51e70-113">Kopieren Sie die neue Anbieter-DLL zusammen mit dem neuen Namen.</span><span class="sxs-lookup"><span data-stu-id="51e70-113">Copy the new provider DLL with the new name alongside the old one.</span></span>
    2.  <span data-ttu-id="51e70-114">Registrieren Sie den neuen Anbieter selbst.</span><span class="sxs-lookup"><span data-stu-id="51e70-114">Self-register the new provider.</span></span>

        <span data-ttu-id="51e70-115">Verwenden Sie z. b. den **regsvr32** **myprov1.dll** -Befehl, um den neuen Anbieter zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="51e70-115">For example, use the **regsvr32** **myprov1.dll** command to register the new provider.</span></span>

    3.  <span data-ttu-id="51e70-116">Kompilieren Sie die neue MOF-Anbieter Registrierung, wodurch die alte Anbieter Registrierung überschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="51e70-116">Compile the new provider registration MOF, thus overwriting the old provider registration.</span></span> <span data-ttu-id="51e70-117">Bis zu diesem Punkt war der alte Anbieter voll funktionsfähig. der neue Anbieter ist nun voll funktionstüchtig.</span><span class="sxs-lookup"><span data-stu-id="51e70-117">Until this point, the old provider was fully functional; now the new provider is fully operational.</span></span>

3.  <span data-ttu-id="51e70-118">Entfernen Sie ggf. die alte Version des Anbieters.</span><span class="sxs-lookup"><span data-stu-id="51e70-118">Remove the old version of the provider, if necessary.</span></span>

    1.  <span data-ttu-id="51e70-119">Heben Sie die Registrierung der alten dll auf.</span><span class="sxs-lookup"><span data-stu-id="51e70-119">Unregister the old DLL.</span></span>

        <span data-ttu-id="51e70-120">Verwenden Sie z. b. den **regsvr32** **/#b0-** Befehl, um die Registrierung der alten dll aufzuheben.</span><span class="sxs-lookup"><span data-stu-id="51e70-120">For example, use the **regsvr32** **/umyprov.dll** command to unregister the old DLL.</span></span>

    2.  <span data-ttu-id="51e70-121">Markieren Sie die alte dll, die beim Neustart gelöscht werden soll, indem Sie " [**muvefileex**](/windows/desktop/api/winbase/nf-winbase-movefileexa)" aufrufen.</span><span class="sxs-lookup"><span data-stu-id="51e70-121">Mark the old DLL to be deleted on reboot by calling [**MoveFileEx**](/windows/desktop/api/winbase/nf-winbase-movefileexa).</span></span>

<span data-ttu-id="51e70-122">Sie können ähnliche Schritte ausführen, um ein Upgrade eines von einem lokalen Server implementierten Anbieters durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="51e70-122">You can take similar steps to upgrade a local server-implemented provider.</span></span>

## <a name="related-topics"></a><span data-ttu-id="51e70-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="51e70-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="51e70-124">Entwickeln eines WMI-Anbieters</span><span class="sxs-lookup"><span data-stu-id="51e70-124">Developing a WMI Provider</span></span>](developing-a-wmi-provider.md)
</dt> <dt>

[<span data-ttu-id="51e70-125">Festlegen von namepace-Sicherheits Deskriptoren</span><span class="sxs-lookup"><span data-stu-id="51e70-125">Setting Namepace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> <dt>

[<span data-ttu-id="51e70-126">Sichern Ihres Anbieters</span><span class="sxs-lookup"><span data-stu-id="51e70-126">Securing Your Provider</span></span>](securing-your-provider.md)
</dt> </dl>

 

 
