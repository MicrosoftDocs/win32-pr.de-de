---
description: Fügen Sie für jedes Kennwort, das vom Benutzer eingegeben werden muss, ein Bearbeitungs Steuerelement in einem Dialogfeld hinzu, in dem der Wert des Kennworts in einer Eigenschaft gespeichert wird.
ms.assetid: aa4ff8b8-cbbb-4b18-83b3-279e52d9f6d3
title: Erstellen der Benutzeroberfläche für die Kenn Wort Eingabe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b37cd7bb9531cbf63a443011656f200717dc0214
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349810"
---
# <a name="authoring-the-user-interface-for-password-input"></a><span data-ttu-id="56c70-103">Erstellen der Benutzeroberfläche für die Kenn Wort Eingabe</span><span class="sxs-lookup"><span data-stu-id="56c70-103">Authoring the User Interface for Password Input</span></span>

<span data-ttu-id="56c70-104">Fügen Sie für jedes Kennwort, das vom Benutzer eingegeben werden muss, ein Bearbeitungs Steuerelement in einem Dialogfeld hinzu, in dem der Wert des Kennworts in einer Eigenschaft gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="56c70-104">For each password that must be entered by the user, add an edit control on a dialog that stores the value of the password into a property.</span></span> <span data-ttu-id="56c70-105">Dieses [Bearbeitungs Steuer](edit-control.md) Element muss über das [Attribut "Password Control](password-control-attribute.md)" verfügen.</span><span class="sxs-lookup"><span data-stu-id="56c70-105">This [edit control](edit-control.md) should have the [Password Control Attribute](password-control-attribute.md).</span></span> <span data-ttu-id="56c70-106">Dies gibt an, dass die eingegebene Eigenschaft ein Kennwort ist und verhindert, dass das Installationsprogramm die Eigenschaft in die Protokolldatei schreibt.</span><span class="sxs-lookup"><span data-stu-id="56c70-106">This specifies that the property entered is a password and prevents the installer from writing the property to the log file.</span></span>

<span data-ttu-id="56c70-107">Die [Steuerelement Attribute](control-attributes.md) für das Kenn Wort Bearbeitungs Steuerelement sind msidbcontrolattributesvisible, msidbcontrolattributesaktiviertes und msidbcontrolattributespasswordinput (1 + 2 + 2097152).</span><span class="sxs-lookup"><span data-stu-id="56c70-107">The [control attributes](control-attributes.md) for the password edit control are msidbControlAttributesVisible, msidbControlAttributesEnabled, and msidbControlAttributesPasswordInput (1 + 2 + 2097152).</span></span> <span data-ttu-id="56c70-108">"X", "Y", "width", "Height" und "Control \_ Next" hängen vom Layout des Steuer Elements im Dialogfeld ab.</span><span class="sxs-lookup"><span data-stu-id="56c70-108">The X, Y, Width, Height, and Control\_Next depend on the layout of the control on the dialog.</span></span>

[<span data-ttu-id="56c70-109">Steuerungs Tabelle</span><span class="sxs-lookup"><span data-stu-id="56c70-109">Control Table</span></span>](control-table.md)



| <span data-ttu-id="56c70-110">Dialog\_</span><span class="sxs-lookup"><span data-stu-id="56c70-110">Dialog\_</span></span> | <span data-ttu-id="56c70-111">Steuerelement\_</span><span class="sxs-lookup"><span data-stu-id="56c70-111">Control\_</span></span>            | <span data-ttu-id="56c70-112">type</span><span class="sxs-lookup"><span data-stu-id="56c70-112">Type</span></span> | <span data-ttu-id="56c70-113">X</span><span class="sxs-lookup"><span data-stu-id="56c70-113">X</span></span>   | <span data-ttu-id="56c70-114">J</span><span class="sxs-lookup"><span data-stu-id="56c70-114">Y</span></span>   | <span data-ttu-id="56c70-115">Breite</span><span class="sxs-lookup"><span data-stu-id="56c70-115">Width</span></span> | <span data-ttu-id="56c70-116">Höhe</span><span class="sxs-lookup"><span data-stu-id="56c70-116">Height</span></span> | <span data-ttu-id="56c70-117">Attribute</span><span class="sxs-lookup"><span data-stu-id="56c70-117">Attributes</span></span> | <span data-ttu-id="56c70-118">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="56c70-118">Property</span></span>         | <span data-ttu-id="56c70-119">Text</span><span class="sxs-lookup"><span data-stu-id="56c70-119">Text</span></span> | <span data-ttu-id="56c70-120">Nächstes Steuerelement \_</span><span class="sxs-lookup"><span data-stu-id="56c70-120">Control\_Next</span></span> | <span data-ttu-id="56c70-121">Hilfe</span><span class="sxs-lookup"><span data-stu-id="56c70-121">Help</span></span> |
|----------|----------------------|------|-----|-----|-------|--------|------------|------------------|------|---------------|------|
| <span data-ttu-id="56c70-122">MyDialog</span><span class="sxs-lookup"><span data-stu-id="56c70-122">MyDialog</span></span> | <span data-ttu-id="56c70-123">Testuserpasswordebug</span><span class="sxs-lookup"><span data-stu-id="56c70-123">TestUserPasswordEdit</span></span> | <span data-ttu-id="56c70-124">Bearbeiten</span><span class="sxs-lookup"><span data-stu-id="56c70-124">Edit</span></span> | <span data-ttu-id="56c70-125">25</span><span class="sxs-lookup"><span data-stu-id="56c70-125">25</span></span>  | <span data-ttu-id="56c70-126">120</span><span class="sxs-lookup"><span data-stu-id="56c70-126">120</span></span> | <span data-ttu-id="56c70-127">300</span><span class="sxs-lookup"><span data-stu-id="56c70-127">300</span></span>   | <span data-ttu-id="56c70-128">20</span><span class="sxs-lookup"><span data-stu-id="56c70-128">20</span></span>     | <span data-ttu-id="56c70-129">2097155</span><span class="sxs-lookup"><span data-stu-id="56c70-129">2097155</span></span>    | <span data-ttu-id="56c70-130">Testuserpassword</span><span class="sxs-lookup"><span data-stu-id="56c70-130">TESTUSERPASSWORD</span></span> |      | <span data-ttu-id="56c70-131">Abbrechen</span><span class="sxs-lookup"><span data-stu-id="56c70-131">Cancel</span></span>        |      |



 

<span data-ttu-id="56c70-132">Fahren Sie mit [dem Sichern der Installation](securing-the-installation.md)fort.</span><span class="sxs-lookup"><span data-stu-id="56c70-132">Continue to [Securing the installation](securing-the-installation.md).</span></span>

 

 



