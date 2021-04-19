---
description: WMI verfügt über mehrere skriptinghilfsobjekte, die die für Skripts erforderlichen Konvertierungen bereitstellen
ms.assetid: 832660b7-2992-4d1f-af16-7b8f0477b187
ms.tgt_platform: multiple
title: Skript Hilfsprogramm
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 028079e49a2007d99b81f7832c4bce3cb016701d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106355614"
---
# <a name="scripting-helper-objects"></a>Skript Hilfsprogramm

WMI verfügt über mehrere skriptinghilfsobjekte, die die für Skripts erforderlichen Konvertierungen bereitstellen

WMI-skriptinghilfsobjekte enthalten Folgendes:

-   [**Swap-DateTime**](swbemdatetime.md)
-   [**Errbemubjectpath**](swbemobjectpath.md)
-   [**Win32 \_ securityDescriptor Helper**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper)

Die Hilfsobjekte unterbrechen zusammengesetzte Datenstrukturen so, dass ein Skript nicht erforderlich ist, um die Struktur zu analysieren, um die Elemente zu erhalten. Beispielsweise kann die **WMI-DateTime** -Struktur nicht direkt angezeigt werden und unterscheidet sich von anderen Windows-DateTime-Datenstrukturen, wie z. b. **VT \_ Date**.

## <a name="swbemdatetime"></a>Swap-DateTime

Das Objekt " [**Swap DateTime**](swbemdatetime.md) " stellt Eigenschaften bereit, die den Tag, den Monat, das Jahr, die Tageszeit usw. analysieren. Außerdem werden Konvertierungs Methoden zum Konvertieren des Windows-Verwaltungsinstrumentation (WMI) DateTime in das bzw. aus dem **VT \_ Date** -und [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) -Format bereitstellt. Für die Internet Explorer-Sicherheitseinstellungen (Internet Explorer, IE) ist das Objekt " **Swap DateTime** " das einzige WMI-Skript Objekt, das für die Initialisierung sicher und sicher für die Skripterstellung markiert ist. Weitere Informationen und Beispiele für Datums-und Zeit Konvertierungen finden Sie unter Datums [-und Uhrzeitangaben](https://www.microsoft.com/technet/scriptcenter/scripts/default.mspx) und im technet scriptcenter-Artikel über die [Zeit (Oh und auch über](https://www.microsoft.com/technet/technetmag/issues/2006/07/ScriptingGuy/default.aspx)Datumsangaben).

## <a name="swbemobjectpath"></a>Errbemubjectpath

Die Eigenschaften von " [**errbewbjectpath**](swbemobjectpath.md) " geben den absoluten Pfad eines Objekts an, aber auch die Teile des WMI-Pfads, wie z. b. Server, Namespace, Klasse oder relativer Pfad. Mit dem-Objekt können Sie die Sicherheit des Pfads festlegen, die Schlüsselwerte der Objekte abrufen, die den Pfad darstellen, ermitteln, ob ein einzelnes Objekt ein Singleton ist usw. Weitere Informationen zum Arbeiten mit WMI-Objekt Pfaden finden Sie unter [beschreiben des Speicher Orts eines WMI-Objekts](describing-the-location-of-a-wmi-object.md).

## <a name="win32_securitydescriptorhelper"></a>Win32 \_ securityDescriptor Helper

Die [**Win32 \_ securitydescriptorhelper**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper) -Klasse konvertiert die Sicherheits Beschreibung eines Sicherungs fähigen Objekts von einem Format in ein anderes.

Viele Objekte, wie z. b. Drucker, WMI-Namespaces, Registrierungsschlüssel oder DCOM-Anwendungen, verfügen über Sicherheits Deskriptoren, die den Zugriff auf das Objekt steuern. Sie können WMI verwenden, um zu ermitteln, wer Zugriff auf diese Objekte hat, indem Sie die dem-Objekt zugeordnete Sicherheits Beschreibung abrufen oder festlegen.

Allerdings können unterschiedliche Methoden Sicherheits Deskriptoren in einem binären Bytearray, einem SDDL-Format ( [Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-string-format) ) oder als eine Instanz von [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)erhalten. Die binäre Bytearray-Form einer Sicherheits Beschreibung sollte nicht manipuliert werden, außer durch die C++-Methoden, die für [sicherheitsbeschreibungervorgänge](/windows/desktop/SecAuthZ/security-descriptor-operations)entworfen wurden. Deskriptoren in SDDL befinden sich in Zeichen folgen, sind aber weiterhin umständlich zu bearbeiten. Das am einfachsten zu änderte Format ist **Win32 \_ securityDescriptor**, weil es eingebettete Objekte für Treuhänder, ACE und sid enthält. Weitere Informationen zur Struktur von Sicherheits Beschreibungen in WMI finden Sie unter [WMI Security Descriptor Objects](wmi-security-descriptor-objects.md). Weitere Informationen zum Durchführen von Konvertierungen finden Sie unter [Ändern der Zugriffssicherheit für Sicherungs fähige Objekte](changing-access-security-on-securable-objects.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Skripterstellung in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script)
</dt> </dl>

 

 
