---
description: Der Medientyp (oder-Modus) beschreibt den Typ der auszutauschenden Informationen, z. b. interaktive Stimme. Eine bestimmte Kommunikationssitzung kann mehrere Medientypen umfassen.
ms.assetid: 2eb140f0-ca07-4e60-b9f3-be2f466f4fca
title: Medientyp für eine Sitzung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc8f5c7743a5d5a85003c99b2ac1abbf13f54168
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104530512"
---
# <a name="media-type-for-a-session"></a><span data-ttu-id="c8704-104">Medientyp für eine Sitzung</span><span class="sxs-lookup"><span data-stu-id="c8704-104">Media Type for a Session</span></span>

<span data-ttu-id="c8704-105">Der Medientyp (oder-Modus) beschreibt den Typ der auszutauschenden Informationen, z. b. interaktive Stimme.</span><span class="sxs-lookup"><span data-stu-id="c8704-105">The media type (or mode) describes the type of information being exchanged, such as interactive voice.</span></span> <span data-ttu-id="c8704-106">Eine bestimmte Kommunikationssitzung kann mehrere Medientypen umfassen.</span><span class="sxs-lookup"><span data-stu-id="c8704-106">A given communications session may involve several media types.</span></span>

<span data-ttu-id="c8704-107">Dienstanbieter machen für TAPI und Anwendungen den Medientyp verfügbar, den Sie unterstützen.</span><span class="sxs-lookup"><span data-stu-id="c8704-107">Service providers expose to TAPI and to applications the media type or types they support.</span></span> <span data-ttu-id="c8704-108">Informationen zum Erwerb dieser Daten finden Sie in der Übersicht über den Geräte [Medientyp](media-type-ovr.md) .</span><span class="sxs-lookup"><span data-stu-id="c8704-108">See the device [media type](media-type-ovr.md) overview for information on acquiring this data.</span></span>

<span data-ttu-id="c8704-109">**TAPI 2. x:** Weitere Informationen finden Sie unter [**linegetcallinfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), [**linesetmediamode**](/windows/win32/api/tapi/nf-tapi-linesetmediamode), [**linemonitormedia**](/windows/win32/api/tapi/nf-tapi-linemonitormedia), [**line \_ monitormedia**](./line-monitormedia.md) Message, [linemediamode \_ Konstanten](./linemediamode--constants.md).</span><span class="sxs-lookup"><span data-stu-id="c8704-109">**TAPI 2.x:** See [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), [**lineSetMediaMode**](/windows/win32/api/tapi/nf-tapi-linesetmediamode), [**lineMonitorMedia**](/windows/win32/api/tapi/nf-tapi-linemonitormedia), [**LINE\_MONITORMEDIA**](./line-monitormedia.md) message, [LINEMEDIAMODE\_ Constants](./linemediamode--constants.md).</span></span>

<span data-ttu-id="c8704-110">**TAPI 3. x:** Siehe [**itcallinfo:: get \_ callinfolong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) with **cil \_ mediatypesavailable**, [**itcallinfo::p UT \_ callinfolong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfolong) with **cil \_ mediatypesavailable**, [**itcallinfochangeevent:: get \_ cause**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfochangeevent-get_cause) (gibt die [**callinfochange- \_ Ursache**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfochange_cause) von **CIC \_ mediaType** zurück), [tapimediatype \_ Konstanten](tapimediatype--constants.md).</span><span class="sxs-lookup"><span data-stu-id="c8704-110">**TAPI 3.x:** See [**ITCallInfo::get\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) with **CIL\_MEDIATYPESAVAILABLE**, [**ITCallInfo::put\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfolong) with **CIL\_MEDIATYPESAVAILABLE**, [**ITCallInfoChangeEvent::get\_Cause**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfochangeevent-get_cause) (returns [**CALLINFOCHANGE\_CAUSE**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfochange_cause) of **CIC\_MEDIATYPE**), [TAPIMEDIATYPE\_ Constants](tapimediatype--constants.md).</span></span>

 

 
