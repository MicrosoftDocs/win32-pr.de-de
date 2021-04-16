---
description: Mit der dvdadm. ChangePassword-Methode wird ein neues Anwendungs Kennwort in der Registrierung gespeichert.
ms.assetid: 58dac785-e20e-4a41-89cf-56644964da19
title: ChangePassword-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bba8bfb9adcecdb88f19f3ac1b8061f93486e269
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481030"
---
# <a name="changepassword-method"></a><span data-ttu-id="ba744-103">ChangePassword-Methode</span><span class="sxs-lookup"><span data-stu-id="ba744-103">ChangePassword Method</span></span>

> [!Note]  
> <span data-ttu-id="ba744-104">Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ba744-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="ba744-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="ba744-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="ba744-106">Mit der- `DVDAdm.ChangePassword` Methode wird ein neues Anwendungs Kennwort in der Registrierung gespeichert.</span><span class="sxs-lookup"><span data-stu-id="ba744-106">The `DVDAdm.ChangePassword` method saves a new application password in the registry.</span></span>

``` syntax
        DVD.DVDAdm.ChangePassword(sUserName, sOld, sNew)
```

## <a name="parameters"></a><span data-ttu-id="ba744-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="ba744-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba744-108"><span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*</span><span class="sxs-lookup"><span data-stu-id="ba744-108"><span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*</span></span>
</dt> <dd>

<span data-ttu-id="ba744-109">Gibt den Anmelde Namen des aktuellen Benutzers als Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="ba744-109">Specifies the current user's logon name as a String.</span></span> <span data-ttu-id="ba744-110">Das msdvdadm-Objekt ignoriert diesen Parameter.</span><span class="sxs-lookup"><span data-stu-id="ba744-110">The MSDVDAdm object ignores this parameter.</span></span> <span data-ttu-id="ba744-111">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="ba744-111">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="ba744-112"><span id="sOld"></span><span id="sold"></span><span id="SOLD"></span>*ter*</span><span class="sxs-lookup"><span data-stu-id="ba744-112"><span id="sOld"></span><span id="sold"></span><span id="SOLD"></span>*sOld*</span></span>
</dt> <dd>

<span data-ttu-id="ba744-113">Gibt das alte Kennwort des Benutzers als Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="ba744-113">Specifies the user's old password as a String.</span></span>

</dd> <dt>

<span data-ttu-id="ba744-114"><span id="sNew"></span><span id="snew"></span><span id="SNEW"></span>*SNEW*</span><span class="sxs-lookup"><span data-stu-id="ba744-114"><span id="sNew"></span><span id="snew"></span><span id="SNEW"></span>*sNew*</span></span>
</dt> <dd>

<span data-ttu-id="ba744-115">Gibt das neue Kennwort des Benutzers als Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="ba744-115">Specifies the user's new password as a String.</span></span> <span data-ttu-id="ba744-116">Darf keine leere Zeichenfolge sein.</span><span class="sxs-lookup"><span data-stu-id="ba744-116">Cannot be an empty string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba744-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ba744-117">Return Value</span></span>

<span data-ttu-id="ba744-118">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="ba744-118">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ba744-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ba744-119">Remarks</span></span>

<span data-ttu-id="ba744-120">Derzeit wird der *sUserName* -Parameter für dieses und alle zugehörigen Methoden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="ba744-120">Currently, the *sUserName* parameter is ignored on this and all related methods.</span></span> <span data-ttu-id="ba744-121">Dies bedeutet, dass Personen, die das Kennwort kennen, die elternebene festlegen können.</span><span class="sxs-lookup"><span data-stu-id="ba744-121">This means that whoever knows the password can set the parental level.</span></span> <span data-ttu-id="ba744-122">Es gibt nur ein Kennwort und eine elternebene für die Anwendung.</span><span class="sxs-lookup"><span data-stu-id="ba744-122">There is only one password and one parental level for the application.</span></span> <span data-ttu-id="ba744-123">Es gibt keine Unterstützung einzelner Benutzer Anmelde Namen oder mehrerer Kenn Wort Verwaltung.</span><span class="sxs-lookup"><span data-stu-id="ba744-123">There is no support for individual user logon names or multiple password management.</span></span> <span data-ttu-id="ba744-124">Zum Erzwingen von Verwaltungs Stufen für Eltern sollten die übergeordneten Elemente das Kennwort festlegen und dann die Jugend Stufe festlegen, die für jüngere Mitglieder der Gruppe von Angehörigen geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="ba744-124">To enforce parental management levels, parents should set the password and then set the parental level appropriate for younger members of the group of relatives.</span></span> <span data-ttu-id="ba744-125">Wenn übergeordnete Elemente eine CD mit Inhalten mit Erwachsener Bewertung anzeigen möchten, können Sie die Ebene ändern und dann wieder ändern, wenn die Anzeige abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="ba744-125">When parents want to view a disc with adult-rated content, they can change the level, and then change it back when they are done viewing.</span></span> <span data-ttu-id="ba744-126">Solange die untergeordneten Elemente das Kennwort nicht kennen, können Sie nur Inhalte an oder unterhalb der festgelegten Ebene ansehen.</span><span class="sxs-lookup"><span data-stu-id="ba744-126">As long as the children do not know the password, they can only watch content at or below the level set for them.</span></span>

## <a name="see-also"></a><span data-ttu-id="ba744-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ba744-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba744-128">**ConfirmPassword**</span><span class="sxs-lookup"><span data-stu-id="ba744-128">**ConfirmPassword**</span></span>](confirmpassword-method.md)
</dt> <dt>

[<span data-ttu-id="ba744-129">Msdvdadm-Objekt</span><span class="sxs-lookup"><span data-stu-id="ba744-129">MSDVDAdm Object</span></span>](msdvdadm-object.md)
</dt> </dl>

 

 



