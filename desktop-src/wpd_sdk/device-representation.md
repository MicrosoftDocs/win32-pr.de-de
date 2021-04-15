---
description: Geräte Darstellung
ms.assetid: bf8b9c67-b023-40ed-97c6-9ca030de610a
title: Geräte Darstellung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c95352c191d3e2d34392f4236b926b81cf65fd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484739"
---
# <a name="device-representation"></a><span data-ttu-id="ea270-103">Geräte Darstellung</span><span class="sxs-lookup"><span data-stu-id="ea270-103">Device Representation</span></span>

<span data-ttu-id="ea270-104">Geräte verfügen über zwei Haupt Verhaltensweisen, die von der WPD-Architektur (Windows Portable Devices) adressiert werden:</span><span class="sxs-lookup"><span data-stu-id="ea270-104">Devices have two main behaviors that are addressed by the Windows Portable Devices (WPD) architecture:</span></span>

-   <span data-ttu-id="ea270-105">Zugreifen auf und Speichern von Inhalten</span><span class="sxs-lookup"><span data-stu-id="ea270-105">Accessing and storing content.</span></span> <span data-ttu-id="ea270-106">Beispielsweise müssen Anwendungen in der Lage sein, einem tragbaren Musikplayer Musikdateien hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="ea270-106">For example, applications must be able to add music files to a portable music player.</span></span>
-   <span data-ttu-id="ea270-107">Programmieren des Geräts.</span><span class="sxs-lookup"><span data-stu-id="ea270-107">Programming the device.</span></span> <span data-ttu-id="ea270-108">Dies schließt einfache Vorgänge ein, z. b. das Ändern von Einstellungen und das Vorbereiten des Geräts für die Datenerfassung oder komplexere Vorgänge wie das Hochladen von Firmware.</span><span class="sxs-lookup"><span data-stu-id="ea270-108">This includes simple operations such as changing settings and preparing the device for data capture, or more complex operations such as uploading firmware.</span></span> <span data-ttu-id="ea270-109">Beispiele hierfür sind das Ausgeben eines Befehls "Bildaufnahme" an eine digitale, immer noch Kamera.</span><span class="sxs-lookup"><span data-stu-id="ea270-109">Examples include issuing a "Take Picture" command to a digital still camera.</span></span>

<span data-ttu-id="ea270-110">In WPD werden diese Verhaltensweisen durch das darstellen des Geräts als Hierarchie von Objekten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="ea270-110">In WPD, these behaviors are described by representing the device as a hierarchy of objects.</span></span> <span data-ttu-id="ea270-111">Die folgende Abbildung zeigt eine WPD-Objektdarstellung für ein Gerät mit mehreren Funktionen, bei dem es sich in diesem Fall um ein Mobiltelefon handelt.</span><span class="sxs-lookup"><span data-stu-id="ea270-111">The following illustration shows a WPD object representation for a multi-function device, which in this case is a mobile phone.</span></span>

![Abbildung der Hierarchie von Objekten für ein Mobiltelefon](images/wpd-overview-figure3.gif)

<span data-ttu-id="ea270-113">Diese Hierarchie veranschaulicht die folgenden Funktionen und Inhalte.</span><span class="sxs-lookup"><span data-stu-id="ea270-113">This hierarchy illustrates the following functionality and contents.</span></span>

<span data-ttu-id="ea270-114">Alitäts</span><span class="sxs-lookup"><span data-stu-id="ea270-114">Functionality:</span></span>

-   <span data-ttu-id="ea270-115">Speicher Objekt.</span><span class="sxs-lookup"><span data-stu-id="ea270-115">Storage object.</span></span> <span data-ttu-id="ea270-116">Dieses Gerät verfügt über Datenspeicher.</span><span class="sxs-lookup"><span data-stu-id="ea270-116">This device has data storage.</span></span>
-   <span data-ttu-id="ea270-117">Kontakt Dienst.</span><span class="sxs-lookup"><span data-stu-id="ea270-117">Contacts Service.</span></span> <span data-ttu-id="ea270-118">Dieser Dienst ist ein funktionales Objekt, das zum Synchronisieren und Speichern von Kontakten auf dem Telefon verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="ea270-118">This service is a functional object that can be used to synchronize and store contacts on the phone.</span></span>
-   <span data-ttu-id="ea270-119">SMS-Dienst.</span><span class="sxs-lookup"><span data-stu-id="ea270-119">SMS Service.</span></span> <span data-ttu-id="ea270-120">Dieser Dienst ist ein funktionales Objekt, das zum Senden, empfangen und Speichern von SMS-Nachrichten verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="ea270-120">This service is a functional object that can be used to send, receive, and store SMS messages.</span></span>

<span data-ttu-id="ea270-121">Inhalte:</span><span class="sxs-lookup"><span data-stu-id="ea270-121">Contents:</span></span>

-   <span data-ttu-id="ea270-122">Medienobjekte.</span><span class="sxs-lookup"><span data-stu-id="ea270-122">Media objects.</span></span> <span data-ttu-id="ea270-123">Dieses Gerät speichert Bild-, Musik-und Videodateien in Ordnern des Speicher Objekts.</span><span class="sxs-lookup"><span data-stu-id="ea270-123">This device stores images, music, and video files in folders on the Storage object.</span></span> <span data-ttu-id="ea270-124">Obwohl die in der Abbildung gezeigten Dateien unter einem Ordner gespeichert werden, kann ein Gerät Inhalte in Ordner unterteilen, die nach dem gespeicherten Medientyp angeordnet sind. beispielsweise Bildordner, Musik Ordner und Videoordner.</span><span class="sxs-lookup"><span data-stu-id="ea270-124">While the files shown in the illustration are stored under one folder, a device can subdivide content into folders organized by the type of media stored; for example, image folders, music folders, and video folders.</span></span>
-   <span data-ttu-id="ea270-125">Contact-Objekte.</span><span class="sxs-lookup"><span data-stu-id="ea270-125">Contact objects.</span></span> <span data-ttu-id="ea270-126">Dieses Gerät speichert Kontaktinformationen (z. b. Name, Telefonnummer und Adresse) als untergeordnete Elemente des Contacts-Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="ea270-126">This device stores contact information (such as name, phone number, and address) as children of the Contacts Service</span></span>
-   <span data-ttu-id="ea270-127">Nachrichten Objekte.</span><span class="sxs-lookup"><span data-stu-id="ea270-127">Message objects.</span></span> <span data-ttu-id="ea270-128">Dieses Gerät speichert SMS-Nachrichten als untergeordnete Elemente des SMS-Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="ea270-128">This device stores SMS messages as children of the SMS Service.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ea270-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ea270-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea270-130">**Anwendungs Übersicht**</span><span class="sxs-lookup"><span data-stu-id="ea270-130">**Application Overview**</span></span>](application-overview.md)
</dt> </dl>

 

 



