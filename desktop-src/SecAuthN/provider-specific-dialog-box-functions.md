---
description: Mit anbieterspezifischen Dialogfeld Funktionen kann ein anbieternetzwerk spezifische Informationen anzeigen und behandeln, indem er die System Dialogfelder ändert oder benutzerdefinierte Dialogfelder anzeigt.
ms.assetid: c9a52867-0a0b-40d8-a09d-2b7bed517e13
title: Dialog Feld Funktionen Provider-Specific
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 567c4dcb9f1fd6c2e289d678cf09b3d0d66e4207
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360765"
---
# <a name="provider-specific-dialog-box-functions"></a><span data-ttu-id="44533-103">Dialog Feld Funktionen Provider-Specific</span><span class="sxs-lookup"><span data-stu-id="44533-103">Provider-Specific Dialog Box Functions</span></span>

<span data-ttu-id="44533-104">Mit anbieterspezifischen Dialogfeld Funktionen kann ein anbieternetzwerk spezifische Informationen anzeigen und behandeln, indem er die System Dialogfelder ändert oder benutzerdefinierte Dialogfelder anzeigt.</span><span class="sxs-lookup"><span data-stu-id="44533-104">Provider-specific dialog box functions enable a provider to display and handle network-specific information by altering system dialog boxes or displaying custom dialog boxes.</span></span>

<span data-ttu-id="44533-105">Im folgenden Dialogfeld können Sie dem Dialogfeld **Eigenschaften** des Datei-Managers Schaltflächen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="44533-105">The following dialog box functions add buttons to the File Manager **Properties** dialog box.</span></span> <span data-ttu-id="44533-106">Der Anbieter kann dann die Ereignisse dieser Schaltflächen verarbeiten, um Netzwerk spezifische Aufgaben auszuführen.</span><span class="sxs-lookup"><span data-stu-id="44533-106">The provider can then handle the events of those buttons to perform network-specific tasks.</span></span> <span data-ttu-id="44533-107">Beachten Sie, dass die Anzahl der Schaltflächen, die hinzugefügt werden können, begrenzt ist.</span><span class="sxs-lookup"><span data-stu-id="44533-107">Note that there is a limit to the number of buttons that can be added.</span></span> <span data-ttu-id="44533-108">Aus diesem Grund sollten Anbieter diese Funktion sparsam verwenden.</span><span class="sxs-lookup"><span data-stu-id="44533-108">Because of this, providers should use this capability sparingly.</span></span> <span data-ttu-id="44533-109">Ein Anbieter kann auch eine Schaltfläche nicht hinzufügen, da der verfügbare Speicherplatz bereits von anderen Anbietern verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="44533-109">Also, a provider may find itself unable to add a button because the available space has been used already by other providers.</span></span> <span data-ttu-id="44533-110">Ein Netzwerkanbieter sollte diese Situation verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="44533-110">A network provider should handle this situation.</span></span>



| <span data-ttu-id="44533-111">Funktion</span><span class="sxs-lookup"><span data-stu-id="44533-111">Function</span></span>                                           | <span data-ttu-id="44533-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="44533-112">Description</span></span>                                                                                                                             |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="44533-113">**Npgetpropertytext**</span><span class="sxs-lookup"><span data-stu-id="44533-113">**NPGetPropertyText**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npgetpropertytext)     | <span data-ttu-id="44533-114">Bestimmt die Namen von Schaltflächen, die zu einem Eigenschaften Dialogfeld für eine bestimmte Ressource hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="44533-114">Determines the names of buttons added to a property dialog box for a specific resource.</span></span><br/>                                      |
| [<span data-ttu-id="44533-115">**Nppropertydialog**</span><span class="sxs-lookup"><span data-stu-id="44533-115">**NPPropertyDialog**</span></span>](/windows/desktop/api/Npapi/nf-npapi-nppropertydialog)       | <span data-ttu-id="44533-116">Wird aufgerufen, wenn ein Benutzer auf eine Schaltfläche klickt, die mithilfe der [**npgetpropertytext**](/windows/desktop/api/Npapi/nf-npapi-npgetpropertytext) -Funktion hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="44533-116">Called when a user clicks a button added by using the [**NPGetPropertyText**](/windows/desktop/api/Npapi/nf-npapi-npgetpropertytext) function.</span></span><br/>               |
| [<span data-ttu-id="44533-117">**Npsearchdialog**</span><span class="sxs-lookup"><span data-stu-id="44533-117">**NPSearchDialog**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npsearchdialog)           | <span data-ttu-id="44533-118">Ermöglicht es Netzwerkanbietern, eigene Suchfunktionen zu implementieren, die über die im **Verbindungs** Dialogfeld bereitgestellten hinausgehen.</span><span class="sxs-lookup"><span data-stu-id="44533-118">Enables network providers to implement their own search functionality beyond that provided in the **Connection** dialog box.</span></span><br/> |
| [<span data-ttu-id="44533-119">**Npformatnetworkname**</span><span class="sxs-lookup"><span data-stu-id="44533-119">**NPFormatNetworkName**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npformatnetworkname) | <span data-ttu-id="44533-120">Ermöglicht Netzwerkanbietern das Formatieren oder andere ändern von Netzwerknamen, bevor Sie dem Benutzer angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="44533-120">Enables network providers to format or otherwise modify network names before they are presented to the user.</span></span><br/>                 |



 

 

 




