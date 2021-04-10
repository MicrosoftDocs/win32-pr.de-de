---
title: Grundlagen der strukturierten Speicherung
description: Der strukturierte Speicher bietet das Äquivalent zu einem kompletten Dateisystem zum Speichern von Objekten.
ms.assetid: 7e2d6211-2ea0-4cad-9388-c789b12446ab
keywords:
- Strukturierter Speicherplatz Halter, Grundlagen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d93b74afd620edca5b6beaa43bde6fff43d7263
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858316"
---
# <a name="structured-storage-fundamentals"></a><span data-ttu-id="7ca11-104">Grundlagen der strukturierten Speicherung</span><span class="sxs-lookup"><span data-stu-id="7ca11-104">Structured Storage Fundamentals</span></span>

<span data-ttu-id="7ca11-105">Der strukturierte Speicher stellt die Entsprechung eines kompletten Dateisystems zum Speichern von Objekten mithilfe der in der folgenden Tabelle aufgeführten Elemente dar.</span><span class="sxs-lookup"><span data-stu-id="7ca11-105">Structured Storage provides the equivalent of a complete file system for storing objects through the elements listed in the following table.</span></span>



| <span data-ttu-id="7ca11-106">Element</span><span class="sxs-lookup"><span data-stu-id="7ca11-106">Element</span></span>                                                                  | <span data-ttu-id="7ca11-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7ca11-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7ca11-108">Strukturierte Speicher Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="7ca11-108">Structured Storage Interfaces</span></span>](structured-storage-interfaces.md)       | <span data-ttu-id="7ca11-109">Die Schnittstellen [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage), [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream), [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes)und [**irootstorage**](/windows/desktop/api/Objidl/nn-objidl-irootstorage) sowie eine Reihe verwandter Schnittstellen –[**IPersistStorage**](/windows/win32/api/objidl/nn-objidl-ipersiststorage), [**ipersistent**](/windows/win32/api/objidl/nn-objidl-ipersist), [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile)und [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream).</span><span class="sxs-lookup"><span data-stu-id="7ca11-109">The [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage), [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream), [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes), and [**IRootStorage**](/windows/desktop/api/Objidl/nn-objidl-irootstorage) interfaces, along with a set of related interfaces —[**IPersistStorage**](/windows/win32/api/objidl/nn-objidl-ipersiststorage), [**IPersist**](/windows/win32/api/objidl/nn-objidl-ipersist), [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile), and [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream).</span></span> |
| [<span data-ttu-id="7ca11-110">Strukturierte Speicher-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="7ca11-110">Structured Storage API Functions</span></span>](structured-storage-api-functions.md) | <span data-ttu-id="7ca11-111">Hilfsobjekte, die eine Implementierung von strukturiertem Speicher und einen zweiten Satz von APIs für Verbund Dateien vereinfachen. Dies ist die com-Implementierung der strukturierten Speicher Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="7ca11-111">Helper APIs that facilitate an implementation of structured storage, as well as a second set of APIs for compound files; that is the COM implementation of the structured storage interfaces.</span></span> <span data-ttu-id="7ca11-112">COM bietet auch eine Reihe unterstützter Strukturen und Enumerationswerte, die zum Organisieren von Parametern für Schnittstellen Methoden und APIs verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7ca11-112">COM also provides a set of supporting structures and enumeration values used to organize parameters for interface methods and APIs.</span></span>                              |
| [<span data-ttu-id="7ca11-113">Strukturierte Speicherzugriffs Modi</span><span class="sxs-lookup"><span data-stu-id="7ca11-113">Structured Storage Access Modes</span></span>](structured-storage-access-modes.md)   | <span data-ttu-id="7ca11-114">Ein Satz von Zugriffs Modi zum Steuern des Zugriffs auf Verbund Dateien.</span><span class="sxs-lookup"><span data-stu-id="7ca11-114">A set of access modes for regulating access to compound files.</span></span>                                                                                                                                                                                                                                                                                                 |



 

 

 