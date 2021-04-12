---
description: Sie können die folgenden Methoden verwenden, um Anwendungs Wiederverwendungs Werte für Ihre COM+-Anwendung zu konfigurieren.
ms.assetid: 8f6a4879-cf4c-4171-8448-bc07371e038c
title: Konfigurieren von com+-Anwendungs Wiederverwendungs Werten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b34c989d81f2e3486adb1d12ec76859a1d28f090
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127560"
---
# <a name="configuring-com-application-recycling-values"></a><span data-ttu-id="fdb50-103">Konfigurieren von com+-Anwendungs Wiederverwendungs Werten</span><span class="sxs-lookup"><span data-stu-id="fdb50-103">Configuring COM+ Application Recycling Values</span></span>

<span data-ttu-id="fdb50-104">Sie können die folgenden Methoden verwenden, um Anwendungs Wiederverwendungs Werte für Ihre COM+-Anwendung zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="fdb50-104">You can use the following methods to configure application recycling values for your COM+ application.</span></span>

> [!Note]  
> <span data-ttu-id="fdb50-105">Eine COM+-Anwendung, die für die Verwendung als Windows-Dienst konfiguriert wurde, kann nicht wieder verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fdb50-105">You cannot recycle a COM+ application that has been configured to run as a Windows service.</span></span> <span data-ttu-id="fdb50-106">Außerdem verfügen Bibliotheksanwendungen über die Eigenschaften zum wieder verwenden und zum Pooling Ihres Host Prozesses.</span><span class="sxs-lookup"><span data-stu-id="fdb50-106">Also, library applications have the recycling and pooling properties of their host process.</span></span>

 

## <a name="component-services-administrative-tool"></a><span data-ttu-id="fdb50-107">Verwaltungs Tool für Komponenten Dienste</span><span class="sxs-lookup"><span data-stu-id="fdb50-107">Component Services Administrative Tool</span></span>

<span data-ttu-id="fdb50-108">Führen Sie die folgenden Schritte aus, um die Anwendungs Wiederverwendung für eine COM+-Anwendung zu konfigurieren:</span><span class="sxs-lookup"><span data-stu-id="fdb50-108">To configure application recycling for a COM+ application, use the following steps:</span></span>

1.  <span data-ttu-id="fdb50-109">Klicken Sie in der Konsolen Struktur des Verwaltungs Programms Komponenten Dienste mit der rechten Maustaste auf die COM+-Serveranwendung, die wieder verwendet werden soll, und klicken Sie dann auf **Eigenschaften**.</span><span class="sxs-lookup"><span data-stu-id="fdb50-109">In the console tree of the Component Services administrative tool, right-click the COM+ server application you want to be recycled and then click **Properties**.</span></span>

2.  <span data-ttu-id="fdb50-110">Geben Sie auf der Registerkarte **Pooling &** Wiederverwendung Werte für **Lebensdauer Limit (Minuten)**, Arbeits **Speicher Limit (KB)**, **Ablauf Timeout (Minuten)**, **Abruf Limit** und **Aktivierungs Limit** ein, abhängig von den Kriterien, die Sie verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="fdb50-110">On the **Pooling & Recycling** tab, enter values for **Lifetime Limit (minutes)**, **Memory Limit (KB)**, **Expiration Timeout (minutes)**, **Call Limit**, and **Activation Limit**, depending on the criteria you want to use.</span></span>

    -   <span data-ttu-id="fdb50-111">**Lebensdauer Limit** gibt die maximale Anzahl von Minuten an, die ein Prozess ausgeführt werden kann, bevor er wieder verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fdb50-111">**Lifetime Limit** indicates the maximum number of minutes a process can run before it's recycled.</span></span> <span data-ttu-id="fdb50-112">Der gültige Bereich liegt zwischen 0 und 30.240 Minuten (21 Tage).</span><span class="sxs-lookup"><span data-stu-id="fdb50-112">The valid range is 0 through 30,240 minutes (21 days).</span></span> <span data-ttu-id="fdb50-113">Die Standard Anzahl von Minuten ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="fdb50-113">The default number of minutes is 0.</span></span>
    -   <span data-ttu-id="fdb50-114">Arbeits **Speicher Limit** gibt die maximale Menge an Prozess Speicherauslastung (in Kilobytes) an, bevor der Prozess wieder verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fdb50-114">**Memory Limit** indicates the maximum amount of process memory usage (in kilobytes) before recycling the process.</span></span> <span data-ttu-id="fdb50-115">Wenn die Speicherauslastung des Prozesses die angegebene Anzahl länger als eine Minute überschreitet, wird der Prozess wieder verwendet.</span><span class="sxs-lookup"><span data-stu-id="fdb50-115">If the process's memory usage exceeds the specified number for longer than one minute, the process is recycled.</span></span> <span data-ttu-id="fdb50-116">Der gültige Bereich liegt zwischen 0 und 1.048.576 KB, und die Standardmenge der Speicherauslastung beträgt 0 KB.</span><span class="sxs-lookup"><span data-stu-id="fdb50-116">The valid range is 0 through 1,048,576 KB, and the default amount of memory usage is 0 KB.</span></span>
    -   <span data-ttu-id="fdb50-117">**Ablauf Timeout** gibt die Anzahl von Minuten an, die gewartet werden soll, bevor das Herunterfahren erzwungen wird, damit alle externen Verweise auf Objekte im Prozess freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="fdb50-117">**Expiration Timeout** indicates the number of minutes to wait, before being forcibly shut down, for the release of all external references to objects in the process.</span></span> <span data-ttu-id="fdb50-118">Der gültige Bereich liegt zwischen 1 und 1440 Minuten (24 Stunden), und das Standard Ablauf Timeout beträgt 15 Minuten.</span><span class="sxs-lookup"><span data-stu-id="fdb50-118">The valid range is 1 through 1440 minutes (24 hours), and the default expiration time-out is 15 minutes.</span></span> <span data-ttu-id="fdb50-119">Dieser Wert wird nur verwendet, wenn bereits festgestellt wurde, dass ein Prozess basierend auf den anderen Kriterien wieder verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fdb50-119">This value is used only when it is already determined that a process will be recycled based on the other criteria.</span></span>
    -   <span data-ttu-id="fdb50-120">" **Aufruf Limit** " gibt die maximale Anzahl von Aufrufen an, die Anwendungs Objekte annehmen können, bevor der Prozess wieder verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fdb50-120">**Call Limit** indicates the maximum number of calls that application objects can accept before recycling the process.</span></span> <span data-ttu-id="fdb50-121">Der gültige Bereich liegt zwischen 0 und 1.048.576 aufrufen, und die Standard Anzahl von Aufrufen beträgt 0.</span><span class="sxs-lookup"><span data-stu-id="fdb50-121">The valid range is 0 through 1,048,576 calls, and the default number of calls is 0.</span></span>
    -   <span data-ttu-id="fdb50-122">**Aktivierungs Limit** gibt die maximale Anzahl von Anwendungs Objekt Aktivierungen an, die vor der Wiederverwendung des Prozesses akzeptiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="fdb50-122">**Activation Limit** indicates the maximum number of application object activations to accept before recycling the process.</span></span> <span data-ttu-id="fdb50-123">Der gültige Bereich liegt zwischen 0 und 1.048.576 Aktivierungen, und die Standard Anzahl von Aktivierungen beträgt 0.</span><span class="sxs-lookup"><span data-stu-id="fdb50-123">The valid range is 0 through 1,048,576 activations, and the default number of activations is 0.</span></span>

    > [!Note]  
    > <span data-ttu-id="fdb50-124">Wenn die Einstellung für die **Lebensdauer**, das Arbeits **Speicherlimit**, das **Aufruflimit** oder der Wert für das **Aktivierungs Limit** auf 0 (Standardwert) festgelegt ist, wird die Anwendungs Wiederverwendung für dieses Kriterium deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="fdb50-124">When the **Lifetime Limit**, **Memory Limit**, **Call Limit**, or **Activation Limit** value is set to 0 (the default value), application recycling for that criterion is disabled.</span></span> <span data-ttu-id="fdb50-125">Wenn alle vier dieser Kriterien auf 0 festgelegt sind, wird die Anwendungs Wiederverwendung für die ausgewählte Anwendung deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="fdb50-125">When all four of these criteria are set to 0, application recycling is disabled for the selected application.</span></span>

     

3.  <span data-ttu-id="fdb50-126">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="fdb50-126">Click **OK**.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="fdb50-127">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="fdb50-127">Visual Basic</span></span>

<span data-ttu-id="fdb50-128">Die folgende Funktion in Microsoft Visual Basic veranschaulicht, wie Sie die Werte für die Anwendungs Wiederverwendung für eine beliebige COM+-Serveranwendung festlegen können, die Sie auswählen.</span><span class="sxs-lookup"><span data-stu-id="fdb50-128">The following function in Microsoft Visual Basic demonstrates how you can set the application recycling values for any COM+ server application that you choose.</span></span> <span data-ttu-id="fdb50-129">Um es aus Visual Basic zu verwenden, fügen Sie einen Verweis auf die com+-admin-Typbibliothek hinzu.</span><span class="sxs-lookup"><span data-stu-id="fdb50-129">To use it from Visual Basic, add a reference to the COM+ Admin Type Library.</span></span>


```VB
Function SetMyApplicationRecycling( _
  strApplicationName As String, _
  lngLifetimeLimit As Long, _
  lngMemoryLimit As Long, _
  lngCallLimit As Long, _
  lngActivationLimit As Long, _
  lngExpirationTimeout As Long _
) As Boolean  ' Return False if any errors occur.

    SetMyApplicationRecycling = False  ' Initialize the function.
    On Error GoTo My_Error_Handler  ' Initialize error handling.

    Dim objCatalog As COMAdmin.COMAdminCatalog
    Dim objAppCollection As COMAdmin.COMAdminCatalogCollection
    Dim objApplication As COMAdmin.COMAdminCatalogObject
    Set objCatalog = CreateObject("COMAdmin.COMAdminCatalog")
    Set objAppCollection = objCatalog.GetCollection("Applications")
    objAppCollection.Populate
    For Each objApplication In objAppCollection
        With objApplication
            If .Name = strApplicationName Then
                .Value("RecycleLifetimeLimit") = lngLifetimeLimit
                .Value("RecycleMemoryLimit") = lngMemoryLimit
                .Value("RecycleCallLimit") = lngCallLimit
                .Value("RecycleActivationLimit") = lngActivationLimit
                .Value("RecycleExpirationTimeout") = lngExpirationTimeout
                MsgBox strApplicationName & _
                  " recycling values are now set to the following: " & _
                  vbNewLine & vbNewLine & _
                  "Lifetime Limit = " & lngLifetimeLimit & vbNewLine & _
                  "Memory Limit = " & lngMemoryLimit & vbNewLine & _
                  "Call Limit = " & lngCallLimit & vbNewLine & _
                  "Activation Limit = " & lngActivationLimit & vbNewLine _
                  & "Expiration Timeout = " & lngExpirationTimeout
                Exit For
            End If
        End With
    Next
    objAppCollection.SaveChanges
    Set objApplication = Nothing
    Set objAppCollection = Nothing
    Set objCatalog = Nothing
    SetMyApplicationRecycling = True  ' Successful end to procedure
    Exit Function
    
My_Error_Handler:  ' Replace with specific error handling.
    MsgBox "Error # " & Err.Number & " (Hex: " & Hex(Err.Number) _
      & ")" & vbNewLine & Err.Description
    Set objApplication = Nothing
    Set objAppCollection = Nothing
    Set objCatalog = Nothing
End Function

```



<span data-ttu-id="fdb50-130">Um die-Funktion zu verwenden, geben Sie einen Zeichen folgen Wert für den Anwendungsnamen und ganzzahlige Werte für die Einstellungen der gewünschten Anwendungs Wiederverwendung an.</span><span class="sxs-lookup"><span data-stu-id="fdb50-130">To use the function, provide a string value for the application name and integer values for the desired application recycling settings.</span></span> <span data-ttu-id="fdb50-131">Der folgende Visual Basic Code zeigt, wie der Wert für " **recyclelifetimelimit** " auf "5", den Wert " **recyclememorylimit** " auf "10", den Wert "RecycleCallLimit" auf 9, den Wert für " **recycleactivationlimit** " 100 auf "9" und den Wert " **recycleexpirationtimeout** " auf 15 </span><span class="sxs-lookup"><span data-stu-id="fdb50-131">The following Visual Basic code shows how to set the **RecycleLifetimeLimit** value to 5, the **RecycleMemoryLimit** value to 10, the **RecycleCallLimit** value to 9, the **RecycleActivationLimit** value to 100, and the **RecycleExpirationTimeout** value to 15.</span></span>


```VB
Sub Main()
    If Not SetMyApplicationRecycling("MyApp", 5, 10, 9, 100, 15) Then
        MsgBox "SetMyApplicationRecycling failed."
    End If
End Sub

```



## <a name="related-topics"></a><span data-ttu-id="fdb50-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fdb50-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fdb50-133">Konzepte der com+-Anwendungs Wiederverwendung</span><span class="sxs-lookup"><span data-stu-id="fdb50-133">COM+ Application Recycling Concepts</span></span>](com--application-recycling-concepts.md)
</dt> </dl>

 

 



