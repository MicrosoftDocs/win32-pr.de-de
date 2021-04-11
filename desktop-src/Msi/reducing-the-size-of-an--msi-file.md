---
description: Entwickler von Windows Installer Paketen bemerken möglicherweise, dass Ihre MSI-Dateien nach wiederholten Änderungen und speichern größer als erwartet werden.
ms.assetid: d5229ef5-0cb5-4daf-8468-0cb653029c1c
title: Reduzieren der Größe einer MSI-Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b5a19c92f0567fc6081d772279ec2cc0b6cafef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959659"
---
# <a name="reducing-the-size-of-an-msi-file"></a><span data-ttu-id="ea675-103">Reduzieren der Größe einer MSI-Datei</span><span class="sxs-lookup"><span data-stu-id="ea675-103">Reducing the Size of an .msi File</span></span>

<span data-ttu-id="ea675-104">Entwickler von Windows Installer Paketen bemerken möglicherweise, dass Ihre MSI-Dateien nach wiederholten Änderungen und speichern größer als erwartet werden.</span><span class="sxs-lookup"><span data-stu-id="ea675-104">Developers of Windows Installer packages may notice their .msi files getting larger than expected after repeated edits and saves.</span></span> <span data-ttu-id="ea675-105">Windows Installer. msi-Dateien sind Verbund Dateien, die Speicher und Streams enthalten und einige der gleichen Speicher Einschränkungen wie OLE-Dokument Dateien aufweisen.</span><span class="sxs-lookup"><span data-stu-id="ea675-105">Windows Installer .msi files are compound files that contain storages and streams, and have some of the same storage limitations as OLE document files.</span></span> <span data-ttu-id="ea675-106">Wenn Sie dieselbe MSI-Datei immer wieder bearbeiten und speichern, wird in der Dateispeicher Platz verschwendet.</span><span class="sxs-lookup"><span data-stu-id="ea675-106">If you edit and save the same .msi file over and over, it creates wasted storage space in the file.</span></span> <span data-ttu-id="ea675-107">Dies betrifft nur Autoren von MSI-Dateien und hat keine Auswirkung auf Windows Installer Benutzer.</span><span class="sxs-lookup"><span data-stu-id="ea675-107">This only affects authors of .msi files and has no effect on Windows Installer users.</span></span> <span data-ttu-id="ea675-108">Entwickler möchten diesen Speicherplatz möglicherweise entfernen, bevor Sie Ihre abschließende MSI-Datei versenden.</span><span class="sxs-lookup"><span data-stu-id="ea675-108">Developers may want to remove this wasted storage space before shipping their final .msi file.</span></span>

<span data-ttu-id="ea675-109">Wenn Sie vergeudeten Speicherplatz entfernen und die endgültige Größe von MSI-Dateien verringern möchten, haben Sie die folgenden Optionen.</span><span class="sxs-lookup"><span data-stu-id="ea675-109">To remove wasted storage space and reduce the final size of .msi files, you have the following options.</span></span>

-   <span data-ttu-id="ea675-110">Exportieren Sie alle Tabellen in der-Datenbank in IDT-Dateien, und importieren Sie Sie dann in eine neue Datenbank.</span><span class="sxs-lookup"><span data-stu-id="ea675-110">Export all of the tables in the database to .idt files, and then import those into a new database.</span></span> <span data-ttu-id="ea675-111">Dadurch wird der kompakteste Speicherplatz erzeugt.</span><span class="sxs-lookup"><span data-stu-id="ea675-111">This produces the most compact storage possible.</span></span>
-   <span data-ttu-id="ea675-112">Verwenden Sie ein Software Dienstprogramm, um den Speicherplatz von OLE-Dokument Dateien zu komprimieren.</span><span class="sxs-lookup"><span data-stu-id="ea675-112">Use a software utility for compacting the storage space of OLE document files.</span></span>

 

 



