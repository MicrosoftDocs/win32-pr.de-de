---
description: Transaktions Attribute können manuell mithilfe des Verwaltungs Tools Komponenten Dienste festgelegt werden, oder Sie können beim Schreiben der Komponente programmgesteuerte Unterstützung für Transaktionen hinzufügen.
ms.assetid: b0d701c7-47ef-4034-873f-dd4428efb4c7
title: Festlegen des Transaktions Attributs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c0690a50f79c77a18b089cec1865dfbb9e7f428
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127393"
---
# <a name="setting-the-transaction-attribute"></a><span data-ttu-id="dd18e-103">Festlegen des Transaktions Attributs</span><span class="sxs-lookup"><span data-stu-id="dd18e-103">Setting the Transaction Attribute</span></span>

<span data-ttu-id="dd18e-104">Transaktions Attribute können manuell mithilfe des Verwaltungs Tools Komponenten Dienste festgelegt werden, oder Sie können beim Schreiben der Komponente programmgesteuerte Unterstützung für Transaktionen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="dd18e-104">You can set transaction attributes manually by using the Component Services administrative tool, or you can add programmatic support for transactions when you write your component.</span></span>

<span data-ttu-id="dd18e-105">Weitere Informationen zu Transaktions Attributwerten finden Sie unter [Konfigurieren von Transaktionen](configuring-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="dd18e-105">For more on transaction attribute values, see [Configuring Transactions](configuring-transactions.md).</span></span>

<span data-ttu-id="dd18e-106">**So legen Sie den Attribut Wert mithilfe des Verwaltungs Tools "Komponenten Dienste" fest**</span><span class="sxs-lookup"><span data-stu-id="dd18e-106">**To set the attribute value by using the Component Services administrative tool**</span></span>

1.  <span data-ttu-id="dd18e-107">Klicken Sie in der Konsolen Struktur mit der rechten Maustaste auf die Komponente, die Sie konfigurieren möchten, und klicken Sie dann auf **Eigenschaften**.</span><span class="sxs-lookup"><span data-stu-id="dd18e-107">In the console tree, right-click the component you want to configure and then click **Properties**.</span></span>

2.  <span data-ttu-id="dd18e-108">Klicken Sie im Dialogfeld Komponenteneigenschaften auf die Registerkarte **Transaktionen** .</span><span class="sxs-lookup"><span data-stu-id="dd18e-108">In the component properties dialog box, click the **Transactions** tab.</span></span>

3.  <span data-ttu-id="dd18e-109">Wählen Sie unter **Transaktionsunterstützung** die Option für den gewünschten Wert aus.</span><span class="sxs-lookup"><span data-stu-id="dd18e-109">Under **Transaction support**, select the option for the value you want.</span></span> <span data-ttu-id="dd18e-110">Der Standardwert für alle Komponenten wird **nicht unterstützt**.</span><span class="sxs-lookup"><span data-stu-id="dd18e-110">The default value for all components is **Not Supported**.</span></span>

4.  <span data-ttu-id="dd18e-111">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="dd18e-111">Click **OK**.</span></span>

<span data-ttu-id="dd18e-112">Sie müssen dieses Verfahren für jede Komponente wiederholen.</span><span class="sxs-lookup"><span data-stu-id="dd18e-112">You must repeat this procedure for each component.</span></span>

## <a name="to-set-the-attribute-value-programmatically"></a><span data-ttu-id="dd18e-113">So legen Sie den Attribut Wert Programm gesteuert fest</span><span class="sxs-lookup"><span data-stu-id="dd18e-113">To set the attribute value programmatically</span></span>

<span data-ttu-id="dd18e-114">Programmierer, die Microsoft Visual Basic verwenden, können das Transaction-Attribut mit **mtstransaktionmode** festlegen, einer Klassenmodul Eigenschaft für ActiveX-DLL-Projekte.</span><span class="sxs-lookup"><span data-stu-id="dd18e-114">Programmers using Microsoft Visual Basic can set the transaction attribute with **MTSTransactionMode**, a class module property for ActiveX DLL projects.</span></span> <span data-ttu-id="dd18e-115">Visual Basic ordnet die Auswahl dem entsprechenden com+-Transaktions Attribut Wert zu und veröffentlicht den Wert in der Typbibliothek der Komponente.</span><span class="sxs-lookup"><span data-stu-id="dd18e-115">Visual Basic maps your selection to the equivalent COM+ transaction attribute value and publishes the value in your component's type library.</span></span>

<span data-ttu-id="dd18e-116">In der folgenden Tabelle wird jeder **mtstransaktionmode** -Konstante Wert dem entsprechenden com+-Transaktionswert zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="dd18e-116">The following table maps each **MTSTransactionMode** constant value to its equivalent COM+ transaction value.</span></span>



| <span data-ttu-id="dd18e-117">Mtstransaktionmode-Konstante</span><span class="sxs-lookup"><span data-stu-id="dd18e-117">MTSTransactionMode constant</span></span>         | <span data-ttu-id="dd18e-118">Com+-Transaktionswert</span><span class="sxs-lookup"><span data-stu-id="dd18e-118">COM+ transaction value</span></span>             |
|-------------------------------------|------------------------------------|
| <span data-ttu-id="dd18e-119">Notanmtsobject (Standard)</span><span class="sxs-lookup"><span data-stu-id="dd18e-119">NotAnMTSObject (default)</span></span><br/> | <span data-ttu-id="dd18e-120">Disabled</span><span class="sxs-lookup"><span data-stu-id="dd18e-120">Disabled</span></span><br/>                |
| <span data-ttu-id="dd18e-121">Notransactions</span><span class="sxs-lookup"><span data-stu-id="dd18e-121">NoTransactions</span></span><br/>           | <span data-ttu-id="dd18e-122">Nicht unterstützt (Standard)</span><span class="sxs-lookup"><span data-stu-id="dd18e-122">Not Supported (default)</span></span><br/> |
| <span data-ttu-id="dd18e-123">"Requirements stransaction"</span><span class="sxs-lookup"><span data-stu-id="dd18e-123">RequiresTransaction</span></span> <br/>     | <span data-ttu-id="dd18e-124">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="dd18e-124">Required</span></span><br/>                |
| <span data-ttu-id="dd18e-125">Usestransaction</span><span class="sxs-lookup"><span data-stu-id="dd18e-125">UsesTransaction</span></span> <br/>         | <span data-ttu-id="dd18e-126">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="dd18e-126">Supported</span></span><br/>               |
| <span data-ttu-id="dd18e-127">Requirements-newtransaction</span><span class="sxs-lookup"><span data-stu-id="dd18e-127">RequiresNewTransaction</span></span> <br/>  | <span data-ttu-id="dd18e-128">Requires New</span><span class="sxs-lookup"><span data-stu-id="dd18e-128">Requires New</span></span><br/>            |



 

<span data-ttu-id="dd18e-129">Der Zugriff auf die **mtstransaktionmode** -Eigenschaft kann auch Programm gesteuert mithilfe der com+-Verwaltungs Bibliothek-API erfolgen.</span><span class="sxs-lookup"><span data-stu-id="dd18e-129">The **MTSTransactionMode** property can also be accessed programmatically by using the COM+ Administration Library API.</span></span>

 

 




