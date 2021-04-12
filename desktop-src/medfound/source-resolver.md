---
description: Quellresolver
ms.assetid: 93eecf10-308b-4bb4-92f9-fd32d6ecdb04
title: Quellresolver
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6a844893b0348546d4fd174b0b24405812efcef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344379"
---
# <a name="source-resolver"></a><span data-ttu-id="f91d9-103">Quellresolver</span><span class="sxs-lookup"><span data-stu-id="f91d9-103">Source Resolver</span></span>

<span data-ttu-id="f91d9-104">Der Source Resolver nimmt einen URL oder Bytedatenstrom und erstellt die entsprechende Medienquelle für den Inhalt.</span><span class="sxs-lookup"><span data-stu-id="f91d9-104">The source resolver takes a URL or byte stream and creates the appropriate media source for that content.</span></span> <span data-ttu-id="f91d9-105">Der Source Resolver ist das Standardverfahren, nach dem Anwendungen Medienquellen erstellen.</span><span class="sxs-lookup"><span data-stu-id="f91d9-105">The source resolver is the standard way for the applications to create media sources.</span></span>

<span data-ttu-id="f91d9-106">Intern verwendet der quellresolver *Handlerobjekte* :</span><span class="sxs-lookup"><span data-stu-id="f91d9-106">Internally, the source resolver uses *handler* objects:</span></span>

-   <span data-ttu-id="f91d9-107">*Schema Handler* nehmen eine URL an und erstellen eine Medienquelle oder einen Bytestream.</span><span class="sxs-lookup"><span data-stu-id="f91d9-107">*Scheme handlers* take a URL and create a media source or a byte stream.</span></span>
-   <span data-ttu-id="f91d9-108">*Byte Datenstrom Handler* nehmen einen Bytestream an und erstellen eine Medienquelle.</span><span class="sxs-lookup"><span data-stu-id="f91d9-108">*Byte stream handlers* take a byte stream and create a media source.</span></span>

<span data-ttu-id="f91d9-109">Sie können einen benutzerdefinierten Handler implementieren und ihn der Registrierung hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="f91d9-109">You can implement a custom handler and add it to the registry.</span></span> <span data-ttu-id="f91d9-110">Schema Handler werden über das URL-Schema registriert, und Byte Datenstrom Handler werden durch die Dateinamenerweiterung oder den MIME-Typ registriert.</span><span class="sxs-lookup"><span data-stu-id="f91d9-110">Scheme handlers are registered by URL scheme, and byte stream handlers are registered by file name extension or MIME type.</span></span>

<span data-ttu-id="f91d9-111">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="f91d9-111">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="f91d9-112">Verwenden des quellresolvers</span><span class="sxs-lookup"><span data-stu-id="f91d9-112">Using the Source Resolver</span></span>](using-the-source-resolver.md)
-   [<span data-ttu-id="f91d9-113">Konfigurieren einer Medienquelle</span><span class="sxs-lookup"><span data-stu-id="f91d9-113">Configuring a Media Source</span></span>](configuring-a-media-source.md)
-   [<span data-ttu-id="f91d9-114">Schema Handler und Byte-Stream Handler</span><span class="sxs-lookup"><span data-stu-id="f91d9-114">Scheme Handlers and Byte-Stream Handlers</span></span>](scheme-handlers-and-byte-stream-handlers.md)

## <a name="related-topics"></a><span data-ttu-id="f91d9-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f91d9-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f91d9-116">Medienquellen</span><span class="sxs-lookup"><span data-stu-id="f91d9-116">Media Sources</span></span>](media-sources.md)
</dt> </dl>

 

 



