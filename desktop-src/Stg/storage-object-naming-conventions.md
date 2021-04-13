---
title: Benennungs Konventionen für Speicher Objekte
description: Speicher-und Streamobjekte werden nach einem Satz von Konventionen benannt.
ms.assetid: 72e87c6a-cce5-4456-8336-c657e65c0a34
keywords:
- Strukturierter Speicherplatz Halter-STG, Grundlagen, Benennungs Konventionen für Speicher Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2e828674f4165bdb54dc2ec06748ab4165e75e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388048"
---
# <a name="storage-object-naming-conventions"></a><span data-ttu-id="c8b84-104">Benennungs Konventionen für Speicher Objekte</span><span class="sxs-lookup"><span data-stu-id="c8b84-104">Storage Object Naming Conventions</span></span>

<span data-ttu-id="c8b84-105">Speicher-und Streamobjekte werden nach einem Satz von Konventionen benannt.</span><span class="sxs-lookup"><span data-stu-id="c8b84-105">Storage and stream objects are named according to a set of conventions.</span></span>

<span data-ttu-id="c8b84-106">Der Name eines Stamm Speicher Objekts ist der tatsächliche Name der Datei im zugrunde liegenden Dateisystem.</span><span class="sxs-lookup"><span data-stu-id="c8b84-106">The name of a root storage object is the actual name of the file in the underlying file system.</span></span> <span data-ttu-id="c8b84-107">Sie entspricht den Konventionen und Einschränkungen, die das Dateisystem auferlegt.</span><span class="sxs-lookup"><span data-stu-id="c8b84-107">It conforms to the conventions and restrictions that the file system imposes.</span></span> <span data-ttu-id="c8b84-108">An speicherbezogene Methoden und Funktionen übergebenen Dateinamen Zeichenfolgen werden an das Dateisystem weitergegeben, nicht interpretiert und unverändert.</span><span class="sxs-lookup"><span data-stu-id="c8b84-108">File name strings passed to storage-related methods and functions are passed on, uninterpreted and unchanged, to the file system.</span></span>

<span data-ttu-id="c8b84-109">Der Name eines geschachtelten Elements, das in einem Speicher Objekt enthalten ist, wird von der-Implementierung des jeweiligen Speicher Objekts verwaltet.</span><span class="sxs-lookup"><span data-stu-id="c8b84-109">The name of a nested element contained within a storage object is managed by the implementation of the particular storage object.</span></span> <span data-ttu-id="c8b84-110">Alle Implementierungen von Speicher Objekten müssen die Länge von 32 Zeichen (einschließlich des **null** -Abschluss Zeichens) unterstützen, obwohl einige Implementierungen längere Namen unterstützen können.</span><span class="sxs-lookup"><span data-stu-id="c8b84-110">All implementations of storage objects must support nested element names 32 characters in length (including the **NULL** terminator), although some implementations might support longer names.</span></span> <span data-ttu-id="c8b84-111">Ob das Speicher Objekt eine Konvertierung durchführt, ist Implementierungs definiert.</span><span class="sxs-lookup"><span data-stu-id="c8b84-111">Whether the storage object does any case conversion is implementation-defined.</span></span> <span data-ttu-id="c8b84-112">Daher müssen Anwendungen, die Elementnamen definieren, Namen auswählen, die akzeptabel sind, unabhängig davon, ob die Groß-/Kleinschreibung konvertiert wird.</span><span class="sxs-lookup"><span data-stu-id="c8b84-112">As a result, applications that define element names must choose names that are acceptable whether or not case conversion is performed.</span></span> <span data-ttu-id="c8b84-113">Die com-Implementierung von Verbund Dateien unterstützt Namen mit einer maximalen Länge von 32 Zeichen und führt keine case-Konvertierung aus.</span><span class="sxs-lookup"><span data-stu-id="c8b84-113">The COM implementation of compound files supports names with a maximum length of 32 characters, and does not perform any case conversion.</span></span>

 

 




