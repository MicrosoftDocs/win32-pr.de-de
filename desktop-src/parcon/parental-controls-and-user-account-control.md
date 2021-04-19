---
description: Eltern Steuerelemente und Benutzerkontensteuerung
ms.assetid: dc7c322a-f534-4dda-8c62-aa628a7b91bc
title: Eltern Steuerelemente und Benutzerkontensteuerung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7798661a7cadc4d497791925c83cdfa684b252a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349203"
---
# <a name="parental-controls-and-user-account-control"></a><span data-ttu-id="5c1d1-103">Eltern Steuerelemente und Benutzerkontensteuerung</span><span class="sxs-lookup"><span data-stu-id="5c1d1-103">Parental Controls and User Account Control</span></span>

<span data-ttu-id="5c1d1-104">Die Benutzerkontensteuerung (User Account Control, UAC) führt zur Anwesenheit geschützter Administrator-und Standard Benutzerkonten.</span><span class="sxs-lookup"><span data-stu-id="5c1d1-104">User Account Control (UAC) will result in presence of Protected Administrator and Standard User accounts.</span></span> <span data-ttu-id="5c1d1-105">Ein geschützter Administrator wird mit denselben Rechten wie ein Standard Benutzer unter normaler Auslastung ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5c1d1-105">A Protected Administrator will run with the same rights as a Standard User under normal usage.</span></span> <span data-ttu-id="5c1d1-106">Für privilegierte Vorgänge:</span><span class="sxs-lookup"><span data-stu-id="5c1d1-106">For privileged operations:</span></span>

-   <span data-ttu-id="5c1d1-107">Ein Standard Benutzer wird im Dialogfeld Anmelde Informationen-Benutzeroberfläche angezeigt, in dem die Eingabe eines Benutzernamens und eines Kennworts für einen geschützten Administrator oder einen integrierten Administrator erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="5c1d1-107">A Standard User will be shown the Credentials User Interface dialog box, which requires the input of a user name and password for a Protected Administrator or built-in Administrator.</span></span>
-   <span data-ttu-id="5c1d1-108">Ein geschützter Administrator wird dem Dialogfeld Benutzeroberfläche zustimmen angezeigt, in dem die Option zum Fortfahren ausgewählt werden muss.</span><span class="sxs-lookup"><span data-stu-id="5c1d1-108">A Protected Administrator will be shown the Consent User Interface dialog box, which requires selection of Allow to proceed.</span></span>

<span data-ttu-id="5c1d1-109">Beachten Sie, dass die UAC pro Prozess implementiert ist, sodass ein Prozess entweder mit erhöhten Rechten ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5c1d1-109">It is important to note that UAC is implemented on a per-process basis, so a process either runs elevated or not.</span></span> <span data-ttu-id="5c1d1-110">Im Allgemeinen ist es aus Sicherheitssicht nicht geeignet, große Anwendungen wie immer erweitert auszuführen.</span><span class="sxs-lookup"><span data-stu-id="5c1d1-110">Generally, it is not suitable from a security standpoint to run large applications as always elevated.</span></span> <span data-ttu-id="5c1d1-111">Für Eltern Steuerelemente sollte Code, der die Einstellungen ändern muss, durch eine von zwei Implementierungs Optionen isoliert werden:</span><span class="sxs-lookup"><span data-stu-id="5c1d1-111">For Parental Controls, code that must modify settings should be isolated by one of two implementation options:</span></span>

1.  <span data-ttu-id="5c1d1-112">Erstellen Sie eine kleine ausführbare Datei für die Einstellungs Verwaltung, die in ihrem Manifest als Administratorrechte gekennzeichnet ist.</span><span class="sxs-lookup"><span data-stu-id="5c1d1-112">Create a small executable for settings management that is marked in its manifest as requiring administrative rights.</span></span> <span data-ttu-id="5c1d1-113">Der Aufruf der ausführbaren Datei bewirkt, dass die Benutzeroberfläche für die Zustimmung oder die Anmelde Informationen angezeigt wird, bevor der Prozess ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="5c1d1-113">Invocation of the executable will cause the Consent or Credentials UI to be shown prior to allowing the process to run.</span></span>
2.  <span data-ttu-id="5c1d1-114">Bereitstellen von COM-Schnittstellen in einer Produkt-dll, die Aufrufe pro UAC-Dokumentation ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="5c1d1-114">Provide COM interfaces in a product DLL that allow for invocation per UAC documentation.</span></span> <span data-ttu-id="5c1d1-115">Dies führt auch dazu, dass die entsprechende Benutzeroberfläche für Zustimmung oder Anmelde Informationen angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="5c1d1-115">This will also cause the appropriate Consent or Credentials UI to be shown.</span></span>

 

 



