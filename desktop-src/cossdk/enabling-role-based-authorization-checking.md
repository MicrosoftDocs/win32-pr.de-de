---
description: Um die rollenbasierte Sicherheit in der com+-Anwendung zu verwenden, müssen Sie zunächst die rollenbasierte Autorisierungs Überprüfung für die Anwendung aktivieren.
ms.assetid: d391a0d4-fe5d-4587-b0b1-b3aa294b7ad7
title: Aktivieren der Role-Based Autorisierungs Überprüfung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c4268c35812af04ed8a0056900e821029274756
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041470"
---
# <a name="enabling-role-based-authorization-checking"></a><span data-ttu-id="c0ea5-103">Aktivieren der Role-Based Autorisierungs Überprüfung</span><span class="sxs-lookup"><span data-stu-id="c0ea5-103">Enabling Role-Based Authorization Checking</span></span>

<span data-ttu-id="c0ea5-104">Um die rollenbasierte Sicherheit in der com+-Anwendung zu verwenden, müssen Sie zunächst die rollenbasierte Autorisierungs Überprüfung für die Anwendung aktivieren.</span><span class="sxs-lookup"><span data-stu-id="c0ea5-104">To use role-based security in your COM+ application, you must first enable role-based authorization checking for the application.</span></span> <span data-ttu-id="c0ea5-105">Dadurch wird sichergestellt, dass Benutzer, die auf die Anwendung zugreifen, auf die Rolle geprüft werden, der Sie angehören, bevor Sie autorisiert werden, etwas in der Anwendung durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="c0ea5-105">This ensures that users who are accessing the application are checked for the role they belong to before they are authorized to do anything in the application.</span></span> <span data-ttu-id="c0ea5-106">Wenn die rollenbasierte Autorisierungs Überprüfung nicht aktiviert ist, wird die rollenbasierte Sicherheit für die Anwendung nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="c0ea5-106">If role-based authorization checking is not enabled, role-based security for the application is not used.</span></span>

<span data-ttu-id="c0ea5-107">**So aktivieren Sie die rollenbasierte Autorisierungs Überprüfung**</span><span class="sxs-lookup"><span data-stu-id="c0ea5-107">**To enable role-based authorization checking**</span></span>

1.  <span data-ttu-id="c0ea5-108">Klicken Sie mit der rechten Maustaste auf die COM+-Anwendung, für die Sie die rollenbasierte Autorisierungs Überprüfung aktivieren, und klicken Sie dann auf **Eigenschaften**.</span><span class="sxs-lookup"><span data-stu-id="c0ea5-108">Right-click the COM+ application for which you are enabling role-based authorization checking, and then click **Properties**.</span></span>

2.  <span data-ttu-id="c0ea5-109">Klicken Sie im Dialogfeld Anwendungseigenschaften auf die Registerkarte **Sicherheit** .</span><span class="sxs-lookup"><span data-stu-id="c0ea5-109">In the application properties dialog box, click the **Security** tab.</span></span>

3.  <span data-ttu-id="c0ea5-110">Wählen Sie unter **Autorisierung** das Kontrollkästchen **Zugriffs Überprüfungen für diese Anwendung erzwingen aus** . Das Deaktivieren des Kontrollkästchens bedeutet, dass für die Anwendung keine rollenbasierte Sicherheit verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c0ea5-110">Under **Authorization**, select the **Enforce access checks for this application** check box; clearing the check box means that role-based security is not used for the application.</span></span>

4.  <span data-ttu-id="c0ea5-111">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="c0ea5-111">Click **OK**.</span></span>

<span data-ttu-id="c0ea5-112">Die ausgewählte Autorisierungs Einstellung wird wirksam, wenn die Anwendung das nächste Mal gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="c0ea5-112">The selected authorization setting takes effect the next time the application is started.</span></span>

 

 



