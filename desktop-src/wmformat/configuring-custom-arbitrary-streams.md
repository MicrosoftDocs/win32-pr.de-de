---
title: Konfigurieren von benutzerdefinierten beliebigen Streams
description: Konfigurieren von benutzerdefinierten beliebigen Streams
ms.assetid: 09b28fd3-a0a3-44d9-b664-7421290abf02
keywords:
- Streams, Konfigurieren von benutzerdefinierten beliebigen Streams
- Codecs, Konfigurieren von benutzerdefinierten beliebigen Streams
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29d5cf3e95a5514ddeede9eb3c25df01ed4cd2ae
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710163"
---
# <a name="configuring-custom-arbitrary-streams"></a><span data-ttu-id="80e4f-105">Konfigurieren von benutzerdefinierten beliebigen Streams</span><span class="sxs-lookup"><span data-stu-id="80e4f-105">Configuring Custom Arbitrary Streams</span></span>

<span data-ttu-id="80e4f-106">Wenn Sie Ihren eigenen beliebigen Datentyp verwenden, müssen Sie einen GUID-Wert erstellen, der als Haupt Bezeichner für den Medientyp fungiert.</span><span class="sxs-lookup"><span data-stu-id="80e4f-106">When using your own arbitrary data type, you must create a GUID value to serve as the major media type identifier for it.</span></span> <span data-ttu-id="80e4f-107">Wenn der Writer einen Stream in einem Profil mit einem Haupttyp findet, der nicht erkannt wird, wird davon ausgegangen, dass es sich bei dem Stream um benutzerdefinierte beliebige Daten handelt.</span><span class="sxs-lookup"><span data-stu-id="80e4f-107">When the writer encounters a stream in a profile with a major type it does not recognize, it assumes that the stream is custom arbitrary data.</span></span> <span data-ttu-id="80e4f-108">Sie akzeptiert Ihre Beispiele, fügt Sie ein und kombiniert Sie mit Beispielen aus anderen Streams in der Datei, ohne die Daten zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="80e4f-108">It will accept your samples, packetize them, and combine them with samples from the other streams in the file without verifying the data in any way.</span></span>

<span data-ttu-id="80e4f-109">Sie können auch eigene GUID-Bezeichner für den Untertyp erstellen, um Unterkategorien Ihrer benutzerdefinierten Daten zu definieren.</span><span class="sxs-lookup"><span data-stu-id="80e4f-109">You can also create your own subtype GUID identifiers to define subcategories of your custom data.</span></span> <span data-ttu-id="80e4f-110">Der Writer ignoriert diese Untertypen vollständig, aber Sie werden im Header Abschnitt der ASF-Datei beibehalten, sodass Ihre Leseanwendung Sie abrufen und Entscheidungen basierend auf diesen treffen kann.</span><span class="sxs-lookup"><span data-stu-id="80e4f-110">The writer will ignore these subtypes completely, but they will be preserved in the header section of the ASF file, so your reading application can retrieve them and make decisions based on them.</span></span>

<span data-ttu-id="80e4f-111">Ein beliebiger Stream erfordert eine Bitrate und ein Puffer Fenster und muss über eine [**WM- \_ \_ Medientyp**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) Struktur mit den Werten verfügen, die mit Ausnahme des Hauptmedien Typs und des Untertyps (bei Verwendung eines) gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="80e4f-111">An arbitrary stream requires a bit rate and buffer window, and must have a [**WM\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) structure with the values cleared except for the major media type and subtype(if using one).</span></span>

## <a name="related-topics"></a><span data-ttu-id="80e4f-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="80e4f-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80e4f-113">**Allgemeine Konfiguration für alle Streams**</span><span class="sxs-lookup"><span data-stu-id="80e4f-113">**Configuration Common to All Streams**</span></span>](configuration-common-to-all-streams.md)
</dt> <dt>

[<span data-ttu-id="80e4f-114">**Konfigurieren beliebiger Streamtypen**</span><span class="sxs-lookup"><span data-stu-id="80e4f-114">**Configuring Arbitrary Stream Types**</span></span>](configuring-arbitrary-stream-types.md)
</dt> <dt>

[<span data-ttu-id="80e4f-115">**Benutzerdefinierte beliebige Datenströme**</span><span class="sxs-lookup"><span data-stu-id="80e4f-115">**Custom Arbitrary Data Streams**</span></span>](custom-arbitrary-data-streams.md)
</dt> </dl>

 

 




