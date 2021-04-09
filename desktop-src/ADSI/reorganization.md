---
title: Neuorganisation
description: 'Die Vertriebsorganisation wurde in eine neue Organisation verschoben: \ 8212; \ 0034; Vertrieb und Support. \ 0034; Julie Bankert wurde zu Vice President herauf gestuft und führt die neue Organisation aus.'
ms.assetid: 38b05d0b-2739-43c2-aac7-7555a5bfbc91
ms.tgt_platform: multiple
keywords:
- Reorganisations-ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 587f3de34738814b34ad250bb00bb7b71121d65c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036307"
---
# <a name="reorganization"></a><span data-ttu-id="7f621-105">Neuorganisation</span><span class="sxs-lookup"><span data-stu-id="7f621-105">Reorganization</span></span>

<span data-ttu-id="7f621-106">Die Vertriebsorganisation wurde in eine neue Organisation verlagert – "Vertrieb und Support".</span><span class="sxs-lookup"><span data-stu-id="7f621-106">The sales organization has moved to a new organization — "Sales and Support."</span></span> <span data-ttu-id="7f621-107">Julie Bankert wurde zu Vice President herauf gestuft und führt die neue Organisation aus.</span><span class="sxs-lookup"><span data-stu-id="7f621-107">Julie Bankert has been promoted to vice president and will lead the new organization.</span></span> <span data-ttu-id="7f621-108">Joe von, der Unternehmens Administrator, muss Vertriebs-ou in eine neue Organisationseinheit, Vertrieb und Support verschieben.</span><span class="sxs-lookup"><span data-stu-id="7f621-108">Joe Worden, the enterprise administrator, must move Sales OU to a new OU, Sales and Support.</span></span>


```VB
Set dom = GetObject("LDAP://DC=Fabrikam,DC=COM")
Set salesSupport = dom.Create("organizationalUnit", "CN=Sales and Support")
Set sales = salesSupport.MoveHere("LDAP://OU=Sales,DC=Fabrikam,DC=COM", vbNullString)
```



<span data-ttu-id="7f621-109">Mit diesem Codebeispiel werden alle Objekte in der Organisationseinheit "Sales", einschließlich der untergeordneten Organisationseinheiten, in die neue Organisationseinheit verschoben.</span><span class="sxs-lookup"><span data-stu-id="7f621-109">With this code example, all objects in the sales organizational unit, including the sub-organizational units, are moved to the new organizational unit.</span></span>

<span data-ttu-id="7f621-110">Nun kann Joe Julie in die Organisationseinheit Vertrieb und Support verschieben.</span><span class="sxs-lookup"><span data-stu-id="7f621-110">Now, Joe can move Julie into the Sales and Support organizational unit.</span></span>


```VB
Set usr = salesSupport.MoveHere("LDAP://CN=Julie Bankert,OU=Sales,OU=Sales and Support,DC=Fabrikam,DC=COM")
usr.Put "title", "Vice President"
usr.SetInfo
```



<span data-ttu-id="7f621-111">Beachten Sie, dass die Verknüpfung "Manager-direkter Bericht" zwischen Julie Bankert und Chris Gray automatisch durch Active Directory aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="7f621-111">Be aware that the manager-direct report link between Julie Bankert and Chris Gray is automatically updated by Active Directory.</span></span>

<span data-ttu-id="7f621-112">**So erstellen Sie einen Active Directory Bericht**</span><span class="sxs-lookup"><span data-stu-id="7f621-112">**To create an Active Directory report**</span></span>

1.  <span data-ttu-id="7f621-113">Öffnen Sie Visual Basic Version 6,0, und wählen Sie bei Aufforderung für den Projekttyp **Daten Projekt** aus.</span><span class="sxs-lookup"><span data-stu-id="7f621-113">Open Visual Basic version 6.0, and when prompted for the project type, select **Data Project**.</span></span>
2.  <span data-ttu-id="7f621-114">Doppelklicken Sie unter **Daten Projekt** auf **Data Environment1**.</span><span class="sxs-lookup"><span data-stu-id="7f621-114">On **Data Project**, double-click **Data Environment1**.</span></span>
3.  <span data-ttu-id="7f621-115">Klicken Sie im Fenster **Daten Umgebung** mit der rechten Maustaste auf das Verbindungs Objekt **(Connection1)** , und wählen Sie **Eigenschaften** aus.</span><span class="sxs-lookup"><span data-stu-id="7f621-115">On the **Data Environment** window, right-click the connection object **(Connection1)** and select **Properties**.</span></span>
4.  <span data-ttu-id="7f621-116">Wählen Sie **OLE DB Anbieter für Microsoft-Verzeichnisdienste aus**, und klicken Sie auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="7f621-116">Select **OLE DB Provider for Microsoft Directory Services**, and click **Next**.</span></span>
5.  <span data-ttu-id="7f621-117">Wählen Sie **integrierte Sicherheit von Windows NT verwenden** aus, und klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="7f621-117">Select **Use Windows NT Integrated security**, and click **OK**.</span></span> <span data-ttu-id="7f621-118">Dadurch wird ein Connection-Objekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="7f621-118">This creates a connection object.</span></span>
6.  <span data-ttu-id="7f621-119">Klicken Sie mit der rechten Maustaste erneut auf das Fenster **Daten Umgebung** , um **Befehl hinzufügen** auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="7f621-119">Right-click the **Data Environment** window again to select **Add Command**.</span></span> <span data-ttu-id="7f621-120">Klicken Sie mit der rechten Maustaste auf **Command1** , und wählen Sie **Eigenschaften** aus.</span><span class="sxs-lookup"><span data-stu-id="7f621-120">Right-click the **Command1** object and select **Properties**.</span></span> <span data-ttu-id="7f621-121">Das folgende Dialogfeld " **Command1-Eigenschaften** " wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7f621-121">The following **Command1 Properties** dialog box will appear.</span></span>

    ![Dialogfeld "Command1-Eigenschaften"](images/adadsi3.png)

7.  <span data-ttu-id="7f621-123">Klicken Sie auf das Optionsfeld **SQL-Anweisung** , und geben Sie Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="7f621-123">Click the **SQL Statement** option button and type the following:</span></span>

    <span data-ttu-id="7f621-124">SELECT Name, telefonienumber from ' LDAP://DC = fabrikam, DC = com ' WHERE objectCategory = ' Person ' and objectClass = ' User '</span><span class="sxs-lookup"><span data-stu-id="7f621-124">SELECT Name,telephoneNumber FROM 'LDAP://DC=Fabrikam,DC=com' WHERE objectCategory='Person' AND objectClass='user'</span></span>

    <span data-ttu-id="7f621-125">Das **Command** -Objekt wird erstellt.</span><span class="sxs-lookup"><span data-stu-id="7f621-125">The **Command** object is created.</span></span> <span data-ttu-id="7f621-126">Fügen Sie dem Bericht das **Befehls** Objekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="7f621-126">Add the **Command** object to the report.</span></span>

8.  <span data-ttu-id="7f621-127">Doppelklicken Sie im **Projekt** Fenster auf **Data Report1** .</span><span class="sxs-lookup"><span data-stu-id="7f621-127">Double-click **Data Report1** from the **Project** window.</span></span>
9.  <span data-ttu-id="7f621-128">Ziehen Sie das **Command1** -Objekt aus dem **DataEnvironment1** -Fenster in den **Detail** Abschnitt des **Datenbericht** Fensters.</span><span class="sxs-lookup"><span data-stu-id="7f621-128">Drag the **Command1** object from the **DataEnvironment1** window to the **Detail** section in the **Data Report** window.</span></span>
10. <span data-ttu-id="7f621-129">Wählen Sie unter **DataReport1-Eigenschaften** für **Daten** Quelle im Pulldownmenü **DataEnvironment1** aus, und wählen Sie im Feld **DataMember** **Command1** aus.</span><span class="sxs-lookup"><span data-stu-id="7f621-129">On **DataReport1 Properties**, for **DataSource**, select **DataEnvironment1** from the pull-down menu, and select **Command1** in the **DataMember** field.</span></span>
11. <span data-ttu-id="7f621-130">Klicken Sie im Projektfenster mit der rechten Maustaste auf **Daten Projekt**, und wählen Sie **dataproject-Eigenschaften** aus.</span><span class="sxs-lookup"><span data-stu-id="7f621-130">On the project window, right-click **Data Project**, and select **DataProject Properties**.</span></span>
12. <span data-ttu-id="7f621-131">Wählen Sie im Dialogfenster **dataproject-Projekteigenschaften** unter **Start Objekt** die Option **DataReport1** aus dem Pulldownmenü aus.</span><span class="sxs-lookup"><span data-stu-id="7f621-131">On the **DataProject - Project Properties** dialog window, under **Startup Object**, select **DataReport1** from the pull-down menu.</span></span> <span data-ttu-id="7f621-132">Klicken Sie zum Speichern auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="7f621-132">Click **OK** to save.</span></span>
13. <span data-ttu-id="7f621-133">Kompilieren</span><span class="sxs-lookup"><span data-stu-id="7f621-133">Compile.</span></span> <span data-ttu-id="7f621-134">Das folgende Dialogfeld **DataReport1** wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7f621-134">The following **DataReport1** dialog box will appear.</span></span>

    ![datareport1 (Dialogfeld)](images/adadsi4.png)

## <a name="related-topics"></a><span data-ttu-id="7f621-136">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7f621-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7f621-137">Beitreten zu heterogenen Daten</span><span class="sxs-lookup"><span data-stu-id="7f621-137">Joining Heterogeneous Data</span></span>](joining-heterogeneous-data.md)
</dt> </dl>

 

 




