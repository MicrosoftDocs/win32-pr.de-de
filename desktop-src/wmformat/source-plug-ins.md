---
title: Quell-Plug-ins
description: Quell-Plug-ins
ms.assetid: 9adc2d42-6273-4af0-b57f-2dde5738ed94
keywords:
- Windows Media-Format-SDK, Quell-Plug-ins
- Advanced Systems Format (ASF), Quell-Plug-ins
- ASF (Advanced Systems Format), Quell-Plug-ins
- Quell-Plug-ins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4822b9110def4e1b758be40310f503fd56a251fd
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "106339870"
---
# <a name="source-plug-ins"></a><span data-ttu-id="d02df-107">Quell-Plug-ins</span><span class="sxs-lookup"><span data-stu-id="d02df-107">Source Plug-ins</span></span>

<span data-ttu-id="d02df-108">Ein Quell-Plug-in ist eine Option, die Entwicklern zur Verfügung steht, die ihr eigenes Speichersystem für Windows Media®-Dateien implementieren möchten.</span><span class="sxs-lookup"><span data-stu-id="d02df-108">A source plug-in is an option available to developers who wish to implement their own storage system for Windows Media® files.</span></span> <span data-ttu-id="d02df-109">Ein Quell-Plug-in ermöglicht dies durch die Implementierung einer COM-Schnittstelle namens **IStream**, bei der es sich um eine Standardschnittstelle zum Bereitstellen von Daten handelt.</span><span class="sxs-lookup"><span data-stu-id="d02df-109">A source plug-in enables this through the implementation of a COM interface called **IStream**, which is a standard interface for providing data.</span></span>

<span data-ttu-id="d02df-110">Das Quell-Plug-in muss als DLL geschrieben werden, und seine Anwesenheit wird dem SDK über einen Registrierungs Eintrag bekannt gemacht.</span><span class="sxs-lookup"><span data-stu-id="d02df-110">The source plug-in should be written as a dll, and its presence is made known to the SDK through a registry entry.</span></span> <span data-ttu-id="d02df-111">Auf diese Weise kann eine beliebige Anzahl von Quell-Plug-Ins implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="d02df-111">There can be any number of source plug-ins implemented this way.</span></span> <span data-ttu-id="d02df-112">Das Quell-Plug-in muss die [**wmkreatestreamforurl**](wmcreatestreamforurl.md) -Funktion exportieren.</span><span class="sxs-lookup"><span data-stu-id="d02df-112">The source plug-in must export the [**WMCreateStreamForURL**](wmcreatestreamforurl.md) function.</span></span>

<span data-ttu-id="d02df-113">Zum Registrieren eines Quell-Plug-ins sollte der folgende Registrierungs Eintrag hinzugefügt werden:</span><span class="sxs-lookup"><span data-stu-id="d02df-113">To register a source plug-in, the following registry entry should be added:</span></span>

<span data-ttu-id="d02df-114">HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Windows Media \\ wmsdk- \\ Quellen</span><span class="sxs-lookup"><span data-stu-id="d02df-114">HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows Media\\WMSDK\\sources</span></span>

<span data-ttu-id="d02df-115">Name = "beliebiger eindeutiger Name"</span><span class="sxs-lookup"><span data-stu-id="d02df-115">Name = "any unique name"</span></span>

<span data-ttu-id="d02df-116">Value = Pfadnamen der Quell-Plug-in-dll</span><span class="sxs-lookup"><span data-stu-id="d02df-116">Value = pathname of the source plug-in dll</span></span>

<span data-ttu-id="d02df-117">Nachdem die dll registriert wurde, kann die Anwendung die **iwmreader:: Open** -Methode (mit der entsprechenden URL als Parameter) verwenden, um auf Streamdaten zuzugreifen, die in Dateien oder benutzerdefinierten Daten Containern gespeichert werden können.</span><span class="sxs-lookup"><span data-stu-id="d02df-117">Once the dll has been registered, the application can use the **IWMReader::Open** method (with the appropriate URL as a parameter) to access stream data, which can be stored in files or user-defined data containers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d02df-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d02df-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d02df-119">**Iwmreader:: Open**</span><span class="sxs-lookup"><span data-stu-id="d02df-119">**IWMReader::Open**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open)
</dt> <dt>

[<span data-ttu-id="d02df-120">**Programmierverzeichnis**</span><span class="sxs-lookup"><span data-stu-id="d02df-120">**Programming Reference**</span></span>](programming-reference.md)
</dt> <dt>

[<span data-ttu-id="d02df-121">**Wmkreatestreamforurl**</span><span class="sxs-lookup"><span data-stu-id="d02df-121">**WMCreateStreamForURL**</span></span>](wmcreatestreamforurl.md)
</dt> </dl>

 

 




