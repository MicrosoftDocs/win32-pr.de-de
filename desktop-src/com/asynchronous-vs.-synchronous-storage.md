---
title: Asynchroner und synchroner Speicher
description: Asynchroner und synchroner Speicher
ms.assetid: de8c50f8-1733-439f-ab53-f98ac21a1fae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 884b8613bebf8ef401f76e4761f48fa0ddd831c2
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104517159"
---
# <a name="asynchronous-and-synchronous-storage"></a><span data-ttu-id="5d598-103">Asynchroner und synchroner Speicher</span><span class="sxs-lookup"><span data-stu-id="5d598-103">Asynchronous and Synchronous Storage</span></span>

<span data-ttu-id="5d598-104">Asynchrone Moniker können auch ein [asynchrones Speicher](/windows/desktop/Stg/asynchronous-storage) Objekt in der [**ibindstatus-Rückruf:: ondataavailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85)) -Benachrichtigung zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="5d598-104">Asynchronous monikers may also return an [Asynchronous Storage](/windows/desktop/Stg/asynchronous-storage) object in the [**IBindStatusCallback::OnDataAvailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85)) notification.</span></span> <span data-ttu-id="5d598-105">Dieses Speicher Objekt erlaubt möglicherweise den Zugriff auf einige der persistenten Daten des Objekts, während die Bindung noch läuft.</span><span class="sxs-lookup"><span data-stu-id="5d598-105">This storage object may allow access to some of the object's persistent data while the binding is still in progress.</span></span> <span data-ttu-id="5d598-106">Ein Client kann zwischen zwei Modi für den Speicher wählen: Blockierung und nicht Blockierung.</span><span class="sxs-lookup"><span data-stu-id="5d598-106">A client can choose between two modes for the storage: blocking and nonblocking.</span></span>

<span data-ttu-id="5d598-107">Im Blockierungs Modus, der mit aktuellen Implementierungen von Speicher Objekten kompatibel ist, wird der-Befehl so lange blockiert, bis Daten empfangen werden, wenn Daten nicht verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="5d598-107">In blocking mode, which is compatible with current implementations of storage objects, if data is unavailable, the call blocks until data arrives.</span></span> <span data-ttu-id="5d598-108">Im nicht blockierenden Modus gibt das Speicher Objekt einen neuen Fehler zurück, der \_ ausstehend ist, wenn Daten nicht verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="5d598-108">In nonblocking mode, rather than blocking the call, the storage object returns a new error E\_PENDING when data is unavailable.</span></span> <span data-ttu-id="5d598-109">Ein Client, der die asynchrone Bindung und den Speicher kennt, bemerkt diesen Fehler und wartet auf weitere Benachrichtigungen ([**ondataavailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85))), um den Vorgang zu wiederholen.</span><span class="sxs-lookup"><span data-stu-id="5d598-109">A client aware of asynchronous binding and storage notes this error and waits for further notifications ([**OnDataAvailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85))) to retry the operation.</span></span> <span data-ttu-id="5d598-110">Ein Client kann zwischen einem synchronen (blockierenden) und asynchronen (nicht blockierenden) Speicher wählen, indem er entscheidet, ob das bindf \_ asyncstorage-Flag im *grfbindf* -Wert festgelegt wird, der an [**IBindStatusCallback:: getbindinfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775058(v=vs.85))zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5d598-110">A client can choose between a synchronous (blocking) and asynchronous (nonblocking) storage by choosing whether to set the BINDF\_ASYNCSTORAGE flag in the *grfBINDF* value returned to [**IBindStatusCallback::GetBindInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775058(v=vs.85)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5d598-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5d598-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5d598-112">Asynchrone Moniker</span><span class="sxs-lookup"><span data-stu-id="5d598-112">Asynchronous Monikers</span></span>](asynchronous-monikers.md)
</dt> </dl>

 

 