---
description: Diese Klasse ist die übergeordnete Klasse für Seiten Fehlerereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: cc349e75-fe81-427e-8cf9-15c76e8e4dad
title: PageFault_V2-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PageFault_V2
api_type:
- NA
api_location: ''
ms.openlocfilehash: a545e8ae7c5afb000c26d89d9359f620fa7a653d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977640"
---
# <a name="pagefault_v2-class"></a>Pagefault \_ v2-Klasse

Diese Klasse ist die übergeordnete Klasse für Seiten Fehlerereignisse.

Die folgende Syntax wird durch den MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[Guid("{3d6fa8d3-fe05-11d0-9dda-00c04fd7ba7c}"), EventVersion(2)]
class PageFault_V2 : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Member

Die **Pagefault \_ v2** -Klasse definiert keine Member.

## <a name="remarks"></a>Bemerkungen

Wenn Sie alle Seiten Fehlerereignisse in einer NT-Kernel Protokollierungs Sitzung aktivieren möchten, geben Sie das Flag für das **Ereignis Ablaufverfolgungsflag \_ \_ \_ Speicher \_ Seiten \_ Fehler** im **enableflags** -Member einer [**Ereignis Ablauf \_ Verfolgungs \_ Eigenschaften**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) -Struktur beim Aufrufen der [**starttrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) -Funktion an. Sie können auch die folgenden Flags angeben:

-   **Ereignis Ablauf \_ Verfolgung Flag für Arbeits \_ \_ Speicher \_ \_ Fehler**
-   **Ereignis \_ Ablaufverfolgungs- \_ Flag \_ virtuelle \_ Zuweisung**

Ereignisablaufverfolgungs-Consumer können eine spezielle Verarbeitung für alle Seiten Fehlerereignisse implementieren, indem Sie die Funktion [**settracecallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) aufrufen und [**pagefehlerguid**](nt-kernel-logger-constants.md) als *pguid* -Parameter angeben. Verwenden Sie die folgenden Ereignis Typen, um das tatsächliche Speicher Ereignis zu identifizieren, wenn Ereignisse verwendet werden.



| Ereignistyp                                                     | BESCHREIBUNG                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ereignis \_ Ablaufverfolgungstyp \_ \_ mm \_ Kuh (Ereignistyp Wert ist 12)<br/> | Copy-on-Write-Ereignis. Die [**Pagefault \_ TypeGroup1**](pagefault-typegroup1.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis. Vor Windows Vista definiert die [**Pagefault \_ transitionfault**](pagefault-transitionfault.md) -MOF-Klasse das Ereignis.     |
| Ereignis \_ Ablaufverfolgungstyp \_ \_ mm \_ DZF (Ereignistyp Wert ist 11)<br/> | Fehler Ereignis nach Bedarf NULL. Die [**Pagefault \_ TypeGroup1**](pagefault-typegroup1.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis. Vor Windows Vista definiert die [**Pagefault \_ transitionfault**](pagefault-transitionfault.md) -MOF-Klasse das Ereignis. |
| Ereignis \_ Ablaufverfolgungstyp \_ \_ mm \_ GPF (Ereignistyp Wert ist 13)<br/> | Fehler Ereignis der Guard-Seite. Die [**Pagefault \_ TypeGroup1**](pagefault-typegroup1.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis. Vor Windows Vista definiert die [**Pagefault \_ transitionfault**](pagefault-transitionfault.md) -MOF-Klasse das Ereignis.  |
| Ereignis \_ Ablaufverfolgungstyp \_ \_ mm \_ HPF (Ereignistyp Wert ist 14)<br/> | Hartes Seiten Fehler Ereignis. Die [**Pagefault \_ TypeGroup1**](pagefault-typegroup1.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis. Vor Windows Vista definiert die [**Pagefault \_ transitionfault**](pagefault-transitionfault.md) -MOF-Klasse das Ereignis.   |
| Ereignis Ablauf \_ Verfolgungs \_ Typ \_ mm \_ tf (Ereignistyp Wert ist 10)<br/>  | Übergangs Fehler Ereignis. Die [**Pagefault \_ TypeGroup1**](pagefault-typegroup1.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis. Vor Windows Vista definiert die [**Pagefault \_ transitionfault**](pagefault-transitionfault.md) -MOF-Klasse das Ereignis.  |
| Ereignis Ablauf \_ Verfolgungs \_ Typ \_ mm \_ AV (Ereignistyp Wert ist 15)<br/>  | Zugriffs Verletzungs Ereignis. Die [**Pagefault \_ TypeGroup1**](pagefault-typegroup1.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.                                                                                                                           |
| Ereignistyp Wert, 32                                           | Hartes Seiten Fehler Ereignis. Die " [**Pagefault \_ Hardfault**](pagefault-hardfault.md) MOF"-Klasse definiert die Ereignisdaten für dieses Ereignis.                                                                                                                               |
| Ereignistyp Wert, 105                                          | Bild Ladevorgang in Auslagerungs Datei Ereignis. Die [**Pagefault \_ imageloadbacked**](pagefault-imageloadbacked.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.                                                                                                          |
| Ereignistyp Wert, 98                                           | Virtuelles Zuordnungs Ereignis. Die " [**virtualzuweisung**](pagefault-virtualalloc.md) MOF"-Klasse definiert die Ereignisdaten für dieses Ereignis.                                                                                                                                |
| Ereignistyp Wert, 99                                           | Virtuelles kostenloses Ereignis. Die " [**virtualzuweisung**](pagefault-virtualalloc.md) MOF"-Klasse definiert die Ereignisdaten für dieses Ereignis.                                                                                                                                      |



 

Sie können den **ProcessID** -und den **ThreadId** -Member des [**Ereignis Ablauf \_ Verfolgungs \_ Headers**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) verwenden, um den fehlerhaften Prozess oder Thread zu identifizieren.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/> |



 

 
