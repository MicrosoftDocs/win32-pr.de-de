---
title: Bindungs Handles
description: Bei der Bindung wird eine logische Verbindung zwischen einem Client Programm und einem Serverprogramm erstellt. Die Informationen, die die Bindung zwischen Client und Server verfasst haben, werden durch eine Struktur dargestellt, die als Bindungs Handle bezeichnet wird.
ms.assetid: 802e6da7-a329-4010-91bd-003ad2169121
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07973deb8319b44a82795a6402ef5e1a9310c2c8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104516847"
---
# <a name="binding-handles"></a><span data-ttu-id="9fc85-104">Bindungs Handles</span><span class="sxs-lookup"><span data-stu-id="9fc85-104">Binding Handles</span></span>

<span data-ttu-id="9fc85-105">Bei der Bindung wird eine logische Verbindung zwischen einem Client Programm und einem Serverprogramm erstellt.</span><span class="sxs-lookup"><span data-stu-id="9fc85-105">Binding is the process of creating a logical connection between a client program and a server program.</span></span> <span data-ttu-id="9fc85-106">Die Informationen, die die Bindung zwischen Client und Server verfasst haben, werden durch eine Struktur dargestellt, die als Bindungs Handle bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="9fc85-106">The information that composes the binding between client and server is represented by a structure called a binding handle.</span></span>

<span data-ttu-id="9fc85-107">Ein Bindungs Handle entspricht einem Datei Handle, das von der fopen-C-Lauf Zeit Bibliotheksfunktion zurückgegeben wird, oder einem Fenster Handle, das von der Funktion " [**kreatewindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) " zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="9fc85-107">A binding handle is analogous to a file handle that the fopen C run-time library function returns, or a window handle that the function [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) returns.</span></span>

<span data-ttu-id="9fc85-108">Wie bei diesen Handles kann Ihre Anwendung nicht direkt auf die Informationen im Bindungs handle zugreifen und diese bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="9fc85-108">As with these handles, your application cannot directly access and manipulate the information in the binding handle.</span></span> <span data-ttu-id="9fc85-109">Die Informationen in einer Bindungs handle-Datenstruktur sind nur für die RPC-Laufzeitbibliotheken verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9fc85-109">The information in a binding handle data structure is available only to the RPC run-time libraries.</span></span> <span data-ttu-id="9fc85-110">Sie stellen das Handle bereit. die Laufzeitbibliotheken greifen auf die entsprechenden Daten zu und bearbeiten Sie.</span><span class="sxs-lookup"><span data-stu-id="9fc85-110">You provide the handle, the run-time libraries access and manipulate the appropriate data.</span></span>

<span data-ttu-id="9fc85-111">In diesem Abschnitt werden die Bindungs Handles in den folgenden Themen erläutert:</span><span class="sxs-lookup"><span data-stu-id="9fc85-111">This section presents a discussion on binding handles in the following topics:</span></span>

-   [<span data-ttu-id="9fc85-112">Typen von Bindungs Handles</span><span class="sxs-lookup"><span data-stu-id="9fc85-112">Types of Binding Handles</span></span>](types-of-binding-handles.md)
-   [<span data-ttu-id="9fc85-113">Client seitige Bindung</span><span class="sxs-lookup"><span data-stu-id="9fc85-113">Client-Side Binding</span></span>](client-side-binding.md)
-   [<span data-ttu-id="9fc85-114">Server seitige Bindung</span><span class="sxs-lookup"><span data-stu-id="9fc85-114">Server-Side Binding</span></span>](server-side-binding.md)
-   [<span data-ttu-id="9fc85-115">Vollständige und teilweise gebundene Handles</span><span class="sxs-lookup"><span data-stu-id="9fc85-115">Fully and Partially Bound Handles</span></span>](fully-and-partially-bound-handles.md)
-   [<span data-ttu-id="9fc85-116">Interpretieren von Bindungs Informationen</span><span class="sxs-lookup"><span data-stu-id="9fc85-116">Interpreting Binding Information</span></span>](interpreting-binding-information.md)
-   [<span data-ttu-id="9fc85-117">Microsoft RPC-Binding-Handle Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="9fc85-117">Microsoft RPC Binding-Handle Extensions</span></span>](microsoft-rpc-binding-handle-extensions.md)
-   [<span data-ttu-id="9fc85-118">Bindungs handle-Funktionen</span><span class="sxs-lookup"><span data-stu-id="9fc85-118">Binding-Handle Functions</span></span>](binding-handle-functions.md)
-   [<span data-ttu-id="9fc85-119">Datenbank des RPC-namens Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="9fc85-119">The RPC Name Service Database</span></span>](the-rpc-name-service-database.md)

 

 