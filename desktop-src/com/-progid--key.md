---
title: ProgID-Schlüssel
description: Eine programmgesteuerte Kennung (ProgID) ist ein Registrierungs Eintrag, der einer CLSID zugeordnet werden kann. Wie die CLSID identifiziert die ProgID eine Klasse, jedoch mit geringerer Genauigkeit, da Sie nicht unbedingt global eindeutig ist.
ms.assetid: f9ef2934-0815-4a6f-9283-8f748eee083b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a9ef64515d2dda4512af0086970cb2ab61b4830
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104039974"
---
# <a name="progid-key"></a><span data-ttu-id="a5ef7-104">ProgID-Schlüssel</span><span class="sxs-lookup"><span data-stu-id="a5ef7-104">ProgID Key</span></span>

<span data-ttu-id="a5ef7-105">Eine programmgesteuerte Kennung (ProgID) ist ein Registrierungs Eintrag, der einer CLSID zugeordnet werden kann.</span><span class="sxs-lookup"><span data-stu-id="a5ef7-105">A programmatic identifier (ProgID) is a registry entry that can be associated with a CLSID.</span></span> <span data-ttu-id="a5ef7-106">Wie die CLSID identifiziert die ProgID eine Klasse, jedoch mit geringerer Genauigkeit, da Sie nicht unbedingt global eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="a5ef7-106">Like the CLSID, the ProgID identifies a class but with less precision because it is not guaranteed to be globally unique.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="a5ef7-107">Registrierungseintrag</span><span class="sxs-lookup"><span data-stu-id="a5ef7-107">Registry Entry</span></span>

<span data-ttu-id="a5ef7-108">**HKEY \_ \_ \\ Software \\ Klassen des lokalen** Computers \\ *{* ProgID *}*</span><span class="sxs-lookup"><span data-stu-id="a5ef7-108">**HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes**\\ *{* ProgID *}*</span></span>



| <span data-ttu-id="a5ef7-109">Registrierungsschlüssel</span><span class="sxs-lookup"><span data-stu-id="a5ef7-109">Registry key</span></span>                            | <span data-ttu-id="a5ef7-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a5ef7-110">Description</span></span>                                                        |
|-----------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="a5ef7-111">**CLSID**</span><span class="sxs-lookup"><span data-stu-id="a5ef7-111">**CLSID**</span></span>](clsid.md)                  | <span data-ttu-id="a5ef7-112">Ordnet eine ProgID einer CLSID zu.</span><span class="sxs-lookup"><span data-stu-id="a5ef7-112">Associates a ProgID with a CLSID.</span></span>                                  |
| [<span data-ttu-id="a5ef7-113">**Einfügbar**</span><span class="sxs-lookup"><span data-stu-id="a5ef7-113">**Insertable**</span></span>](insertable-progid.md) | <span data-ttu-id="a5ef7-114">Gibt an, dass diese Klasse in OLE 2-Containern einfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="a5ef7-114">Indicates that this class is insertable in OLE 2 containers.</span></span>       |
| [<span data-ttu-id="a5ef7-115">**Protokoll**</span><span class="sxs-lookup"><span data-stu-id="a5ef7-115">**Protocol**</span></span>](protocol.md)            | <span data-ttu-id="a5ef7-116">Gibt an, dass diese OLE 2-Klasse in OLE 1-Containern einfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="a5ef7-116">Indicates that this OLE 2 class is insertable in OLE 1 containers.</span></span> |
| [<span data-ttu-id="a5ef7-117">**Shell**</span><span class="sxs-lookup"><span data-stu-id="a5ef7-117">**Shell**</span></span>](shell.md)                  | <span data-ttu-id="a5ef7-118">Bietet Informationen zum Drucken von Windows 3,1-Shell und zum **Öffnen von Dateien** .</span><span class="sxs-lookup"><span data-stu-id="a5ef7-118">Provides Windows 3.1 shell printing and **File Open** information.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="a5ef7-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a5ef7-119">Remarks</span></span>

<span data-ttu-id="a5ef7-120">Eine ProgID kann in Programmier Situationen verwendet werden, in denen eine CLSID nicht verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="a5ef7-120">You can use a ProgID in programming situations where it is not possible to use a CLSID.</span></span> <span data-ttu-id="a5ef7-121">ProgIDs sollten nicht in der Benutzeroberfläche angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="a5ef7-121">ProgIDs should not appear in the user interface.</span></span> <span data-ttu-id="a5ef7-122">ProgIDs sind nicht garantiert eindeutig und können daher nur verwendet werden, wenn Namenskonflikte verwaltbar sind.</span><span class="sxs-lookup"><span data-stu-id="a5ef7-122">ProgIDs are not guaranteed to be unique, so they can be used only where name collisions are manageable.</span></span>

<span data-ttu-id="a5ef7-123">Das Format einer ProgID ist <*Programm*>. <*Component*>. <*Version*>, getrennt durch Punkte und ohne Leerzeichen, wie in Word.Doc"beent. 6".</span><span class="sxs-lookup"><span data-stu-id="a5ef7-123">The format of a ProgID is <*Program*>.<*Component*>.<*Version*>, separated by periods and with no spaces, as in Word.Document.6.</span></span> <span data-ttu-id="a5ef7-124">Die ProgID muss die folgenden Anforderungen erfüllen:</span><span class="sxs-lookup"><span data-stu-id="a5ef7-124">The ProgID must comply with the following requirements:</span></span>

-   <span data-ttu-id="a5ef7-125">Es sind nicht mehr als 39 Zeichen vorhanden.</span><span class="sxs-lookup"><span data-stu-id="a5ef7-125">Have no more than 39 characters.</span></span>
-   <span data-ttu-id="a5ef7-126">Enthalten keine Interpunktions Zeichen (einschließlich Unterstriche), mit Ausnahme von mindestens einem Zeitraum.</span><span class="sxs-lookup"><span data-stu-id="a5ef7-126">Contain no punctuation (including underscores) except one or more periods.</span></span>
-   <span data-ttu-id="a5ef7-127">Beginnen Sie nicht mit einer Ziffer.</span><span class="sxs-lookup"><span data-stu-id="a5ef7-127">Not start with a digit.</span></span>
-   <span data-ttu-id="a5ef7-128">Unterscheiden Sie sich vom Klassennamen jeder OLE 1-Anwendung, einschließlich der OLE 1-Version der gleichen Anwendung (sofern vorhanden).</span><span class="sxs-lookup"><span data-stu-id="a5ef7-128">Be different from the class name of any OLE 1 application, including the OLE 1 version of the same application, if there is one.</span></span>

<span data-ttu-id="a5ef7-129">Da die ProgID nicht in der Benutzeroberfläche angezeigt werden sollte, können Sie einen anzeigbaren Namen abrufen, indem Sie [**IOleObject:: GetUserType**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="a5ef7-129">Because the ProgID should not appear in the user interface, you can obtain a displayable name by calling [**IOleObject::GetUserType**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype).</span></span> <span data-ttu-id="a5ef7-130">Siehe auch [**olereggetusertype**](/windows/desktop/api/Ole2/nf-ole2-olereggetusertype).</span><span class="sxs-lookup"><span data-stu-id="a5ef7-130">Also, see [**OleRegGetUserType**](/windows/desktop/api/Ole2/nf-ole2-olereggetusertype).</span></span>

<span data-ttu-id="a5ef7-131">Der Schlüssel **HKEY- \_ \_ \\ Software \\ Klassen für lokale Computer** entspricht dem Stamm Schlüssel der **HKEY- \_ Klassen \_** , der für die Kompatibilität mit früheren Versionen von com beibehalten wurde.</span><span class="sxs-lookup"><span data-stu-id="a5ef7-131">The **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes** key corresponds to the **HKEY\_CLASSES\_ROOT** key, which was retained for compatibility with earlier versions of COM.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a5ef7-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a5ef7-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a5ef7-133">**IOleObject:: GetUserType**</span><span class="sxs-lookup"><span data-stu-id="a5ef7-133">**IOleObject::GetUserType**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype)
</dt> <dt>

[<span data-ttu-id="a5ef7-134">**Olereggetusertype**</span><span class="sxs-lookup"><span data-stu-id="a5ef7-134">**OleRegGetUserType**</span></span>](/windows/desktop/api/Ole2/nf-ole2-olereggetusertype)
</dt> </dl>

 

 




