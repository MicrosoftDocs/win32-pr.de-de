---
description: Vorteile von Multimedia Streaming
ms.assetid: 01020ad5-430d-4b4d-8de3-bcc81270e132
title: Vorteile von Multimedia Streaming
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd907d9b8e91cb61709479a2d600323d6d420958
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104132157"
---
# <a name="advantages-of-multimedia-streaming"></a><span data-ttu-id="a9af1-103">Vorteile von Multimedia Streaming</span><span class="sxs-lookup"><span data-stu-id="a9af1-103">Advantages of Multimedia Streaming</span></span>

> [!Note]  
> <span data-ttu-id="a9af1-104">Diese APIs sind veraltet.</span><span class="sxs-lookup"><span data-stu-id="a9af1-104">These APIs are deprecated.</span></span> <span data-ttu-id="a9af1-105">Anwendungen sollten den [**Beispiel-Grabber**](sample-grabber-filter.md) Filter verwenden oder einen benutzerdefinierten Filter implementieren, um Daten aus einem DirectShow-Filter Diagramm zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="a9af1-105">Applications should use the [**Sample Grabber**](sample-grabber-filter.md) filter or implement a custom filter to get data from a DirectShow filter graph.</span></span>

 

<span data-ttu-id="a9af1-106">Wenn Entwickler in Ihren Anwendungen multimediastreaming verwenden, wird die Menge der erforderlichen Format spezifischen Programmierung erheblich reduziert.</span><span class="sxs-lookup"><span data-stu-id="a9af1-106">When developers use multimedia streaming in their applications, it greatly reduces the amount of format-specific programming needed.</span></span> <span data-ttu-id="a9af1-107">In der Regel muss eine Anwendung, die Mediendaten aus einer Datei oder Hardware Quelle abrufen muss, alles über das Datenformat und das Hardware Gerät wissen.</span><span class="sxs-lookup"><span data-stu-id="a9af1-107">Typically, an application that must obtain media data from a file or hardware source must know everything about the data format and the hardware device.</span></span> <span data-ttu-id="a9af1-108">Die Anwendung muss die Verbindung, die Übertragung von Daten, die erforderliche Datenkonvertierung und das tatsächliche Daten Rendering oder den Dateispeicher verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="a9af1-108">The application must handle the connection, transfer of data, any necessary data conversion, and the actual data rendering or file storage.</span></span> <span data-ttu-id="a9af1-109">Da sich jedes Format und jedes Gerät geringfügig unterscheiden, ist dieser Prozess häufig komplex und mühsam.</span><span class="sxs-lookup"><span data-stu-id="a9af1-109">Because each format and device is slightly different, this process is often complex and cumbersome.</span></span> <span data-ttu-id="a9af1-110">Das Multimedia-Streaming hingegen aushandiert die Übertragung und Konvertierung von Daten aus der Quelle in die Anwendung automatisch.</span><span class="sxs-lookup"><span data-stu-id="a9af1-110">Multimedia streaming, on the other hand, automatically negotiates the transfer and conversion of data from the source to the application.</span></span> <span data-ttu-id="a9af1-111">Die streamingschnittstellen stellen eine einheitliche und vorhersagbare Methode des Datenzugriffs und-Steuer Elements bereit, die es einer Anwendung erleichtert, die Daten unabhängig von ihrer ursprünglichen Quelle oder Ihrem ursprünglichen Format wiederzugeben.</span><span class="sxs-lookup"><span data-stu-id="a9af1-111">The streaming interfaces provide a uniform and predictable method of data access and control, which makes it easy for an application to play back the data, regardless of its original source or format.</span></span>

<span data-ttu-id="a9af1-112">Die folgenden Schritte zeigen, wie Streaming von einem Hardware Gerät zur gerenderten Wiedergabe implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="a9af1-112">The following steps show how to implement streaming, from hardware device to rendered playback.</span></span>

1.  <span data-ttu-id="a9af1-113">Eine Quelle von Videodaten, z. b. DirectShow, macht die streamingschnittstellen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a9af1-113">A source of video data, such as DirectShow, exposes the streaming interfaces.</span></span>
2.  <span data-ttu-id="a9af1-114">Der Anwendungsentwickler verwendet die Multimedia-streamingschnittstellen zum Verarbeiten der Datenformat Konvertierung.</span><span class="sxs-lookup"><span data-stu-id="a9af1-114">The application developer uses the multimedia streaming interfaces to handle data format conversion.</span></span>
3.  <span data-ttu-id="a9af1-115">Der Anwendungsentwickler verwendet die DirectDraw-Schnittstellen, um die resultierenden Daten zu erzeugen.</span><span class="sxs-lookup"><span data-stu-id="a9af1-115">The application developer uses the DirectDraw interfaces to render the resulting data.</span></span>

<span data-ttu-id="a9af1-116">Die Spezifikation für Multimedia-Streams besteht aus mehreren Schnittstellen. jede Schnittstelle enthält Methoden, die einen bestimmten Aspekt des streamingprozesses Steuern oder einen bestimmten Datentyp verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="a9af1-116">The specification for multimedia streams comprises several interfaces; each interface includes methods that control a certain aspect of the streaming process or handle a certain type of data.</span></span> <span data-ttu-id="a9af1-117">Weitere Informationen finden Sie [in der Liste der multimediastreaming-Schnittstellen](list-of-multimedia-streaming-interfaces.md) .</span><span class="sxs-lookup"><span data-stu-id="a9af1-117">See [List of Multimedia Streaming Interfaces](list-of-multimedia-streaming-interfaces.md) for additional information.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a9af1-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a9af1-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9af1-119">Informationen zur multimediastreamingarchitektur</span><span class="sxs-lookup"><span data-stu-id="a9af1-119">About the Multimedia Streaming Architecture</span></span>](about-the-multimedia-streaming-architecture.md)
</dt> </dl>

 

 



