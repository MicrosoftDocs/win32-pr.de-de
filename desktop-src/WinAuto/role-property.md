---
title: Role-Eigenschaft
description: Die Role-Eigenschaft beschreibt das Benutzeroberflächen Element eines Objekts. Alle-Objekte unterstützen die Role-Eigenschaft.
ms.assetid: f6abf95b-a77a-406d-9ca0-4663adc8245f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f2b285d9242542f83c6b4478df93e888a7a23cd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106339193"
---
# <a name="role-property"></a><span data-ttu-id="cefd0-104">Role-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="cefd0-104">Role Property</span></span>

<span data-ttu-id="cefd0-105">Die **Role** -Eigenschaft beschreibt das Benutzeroberflächen Element eines Objekts.</span><span class="sxs-lookup"><span data-stu-id="cefd0-105">The **Role** property describes an object's user interface element.</span></span> <span data-ttu-id="cefd0-106">Alle-Objekte unterstützen die **Role** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="cefd0-106">All objects support the **Role** property.</span></span>

<span data-ttu-id="cefd0-107">In vielen Fällen ist die Rolle des Objekts offensichtlich.</span><span class="sxs-lookup"><span data-stu-id="cefd0-107">In many cases, the object's role is obvious.</span></span> <span data-ttu-id="cefd0-108">Beispielsweise verfügen Windows über die Rolle " [**Rollen \_ System \_**](object-roles.md) " und die Schaltflächen "Rollensystem" über die [**\_ \_ PUSHBUTTON**](object-roles.md) -Rolle.</span><span class="sxs-lookup"><span data-stu-id="cefd0-108">For example, windows have the [**ROLE\_SYSTEM\_WINDOW**](object-roles.md) role and push buttons have the [**ROLE\_SYSTEM\_PUSHBUTTON**](object-roles.md) role.</span></span>

<span data-ttu-id="cefd0-109">Die **Role** -Eigenschaft wird durch Aufrufen von [**ibarrierefreie:: get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)abgerufen.</span><span class="sxs-lookup"><span data-stu-id="cefd0-109">The **Role** property is retrieved by calling [**IAccessible::get\_accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole).</span></span>

## <a name="identifying-an-objects-role"></a><span data-ttu-id="cefd0-110">Identifizieren der Rolle eines Objekts</span><span class="sxs-lookup"><span data-stu-id="cefd0-110">Identifying an Object's Role</span></span>

<span data-ttu-id="cefd0-111">Microsoft Active Accessibility stellt [Rollen Konstanten](object-roles.md)bereit, die in Oleacc. h definiert sind und die allgemeine Objekt Rollen identifizieren.</span><span class="sxs-lookup"><span data-stu-id="cefd0-111">Microsoft Active Accessibility provides [role constants](object-roles.md), defined in oleacc.h, that identify common object roles.</span></span> <span data-ttu-id="cefd0-112">Es wird empfohlen, dass Server Entwickler diese vordefinierten Rollen Werte verwenden.</span><span class="sxs-lookup"><span data-stu-id="cefd0-112">It is recommended that server developers use these predefined role values.</span></span> <span data-ttu-id="cefd0-113">Wenn eine vordefinierte Rollen Konstante zurückgegeben wird, verwenden Clients die [**getroletext**](/windows/desktop/api/Oleacc/nf-oleacc-getroletexta) -Funktion, um eine lokalisierte Zeichenfolge abzurufen, die die Rolle beschreibt.</span><span class="sxs-lookup"><span data-stu-id="cefd0-113">If a predefined role constant is returned, clients use the [**GetRoleText**](/windows/desktop/api/Oleacc/nf-oleacc-getroletexta) function to retrieve a localized string that describes the role.</span></span>

<span data-ttu-id="cefd0-114">Verwenden Sie für Animations Steuerelemente wie das beim Kopieren von Dateien angezeigte Animations Steuerelement die [**\_ \_ Animation des Rollen Systems**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="cefd0-114">For animation controls, such as the animation control displayed when copying files, use [**ROLE\_SYSTEM\_ANIMATION**](object-roles.md).</span></span> <span data-ttu-id="cefd0-115">Grafiken, die gelegentlich animiert werden, werden als [**Rollen \_ System- \_ Grafik**](object-roles.md) beschrieben, wobei die Eigenschaft [**State**](state-property.md) auf [**State \_ System \_ animiert**](object-state-constants.md)festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="cefd0-115">Graphics that are occasionally animated are described as [**ROLE\_SYSTEM\_GRAPHIC**](object-roles.md) with the [**State**](state-property.md) property set to [**STATE\_SYSTEM\_ANIMATED**](object-state-constants.md).</span></span>

<span data-ttu-id="cefd0-116">Beachten Sie, dass einige Rollen nicht leicht zu beschreiben sind.</span><span class="sxs-lookup"><span data-stu-id="cefd0-116">Note that some roles are not easy to describe.</span></span> <span data-ttu-id="cefd0-117">Beispielsweise ermöglicht die Ansicht "großes Symbol" eines Ordners eine beliebige Anordnung von Symbolen, sodass seine Rolle als [**Rollen \_ System \_ Gruppierung**](object-roles.md)beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="cefd0-117">For example, a folder's large-icon view allows arbitrary arrangement of icons, so its role could be described as [**ROLE\_SYSTEM\_GROUPING**](object-roles.md).</span></span> <span data-ttu-id="cefd0-118">Oder ein Steuerelement, das Elemente in festgelegten Zeilen und Spalten bereitstellt, kann über die [**Rollen \_ System- \_ Tabellen**](object-roles.md) Rolle verfügen.</span><span class="sxs-lookup"><span data-stu-id="cefd0-118">Or, a control that provides items in fixed rows and columns could have the [**ROLE\_SYSTEM\_TABLE**](object-roles.md) role.</span></span> <span data-ttu-id="cefd0-119">Da eine Rolle verwendet wird, um das Verwendungs Modell an einen Endbenutzer zu übermitteln, ist es wichtig, die entsprechende Rolle zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="cefd0-119">Since a role is used to communicate the use model to an end user, it is important to use the appropriate role.</span></span> <span data-ttu-id="cefd0-120">Wenn das Steuerelement z. b. wie eine Schaltfläche funktioniert, verwenden Sie das [**Rollen \_ System- \_ PUSHBUTTON**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="cefd0-120">For example, if your control acts like a button, then use [**ROLE\_SYSTEM\_PUSHBUTTON**](object-roles.md).</span></span>

 

 




