---
title: Programmier Richtlinien für Remotedesktopdienste
description: Themen, in denen Richtlinien zum Entwickeln von Anwendungen in einer Remotedesktopdienste Umgebung bereitgestellt werden.
ms.assetid: e0cd52c5-40d7-4a48-9d10-fdbcea46a5a0
ms.tgt_platform: multiple
keywords:
- Remotedesktopdienste Remotedesktopdienste, Programmier Richtlinien
- Programmier Richtlinien Remotedesktopdienste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e767740a2f279c90ce4f0eb37c49919749465ad1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106339495"
---
# <a name="remote-desktop-services-programming-guidelines"></a>Programmier Richtlinien für Remotedesktopdienste

Die meisten vorhandenen Windows-basierten 32-Bit-oder 64-Bit-Anwendungen werden "unverändert" in einer Remotedesktopdienste-Umgebung (ehemals "Terminal Services" genannt) ausgeführt. Einige Anwendungen funktionieren jedoch ordnungsgemäß und funktionieren gut in einer Remotedesktopdienste Umgebung, andere hingegen nicht. Die folgenden Themen bieten Richtlinien für die Entwicklung von Anwendungen in einer Remotedesktopdienste Umgebung.

## <a name="in-this-section"></a>In diesem Abschnitt

<dl> <dt>

[Richtlinien für mehrere Benutzer](multiple-user-guidelines.md)
</dt> <dd>

Richtlinien für die Entwicklung von Anwendungen für mehrere Benutzer in einer Remotedesktopdienste Umgebung.

</dd> <dt>

[Leistungsrichtlinien](performance-guidelines.md)
</dt> <dd>

Richtlinien für die Entwicklung von Anwendungen, die in einer Remotedesktopdienste Umgebung eine gute Leistung erbringen.

</dd> <dt>

[Allgemeine Programmier Richtlinien](general-programming-guidelines.md)
</dt> <dd>

Richtlinien für die Entwicklung von Anwendungen in einer Remotedesktopdienste Umgebung.

</dd> </dl>

Viele dieser Richtlinien sind gute Programmierverfahren, die Anwendungen profitieren, die in jeder Windows-Umgebung ausgeführt werden. Einige empfohlene Optimierungen, wie z. b. das Einschränken von grafischen Effekten, sind jedoch Optimierungen, die Sie nur dann wünschen, wenn Ihre Anwendung unter Remotedesktopdienste ausgeführt wird. Ein Codebeispiel, in dem gezeigt wird, wie eine Remotedesktopdienste Umgebung erkannt wird, finden Sie unter [erkennen der Remotedesktopdienste Umgebung](detecting-the-terminal-services-environment.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>


</dt> <dt>

[Terminal Dienste sind jetzt Remotedesktopdienste](terminal-services-is-now-remote-desktop-services.md)
</dt> <dt>

[Format der administrativen Vorlagen Datei](/previous-versions/windows/desktop/Policy/administrative-template-file-format)
</dt> <dt>

[Sicherheit und Zugriffsrechte für den Registrierungsschlüssel](/windows/desktop/SysInfo/registry-key-security-and-access-rights)
</dt> <dt>

[Registrierungs Strukturen](/windows/desktop/SysInfo/registry-hives)
</dt> <dt>

[Sicherheitsbeschreibungen](/windows/desktop/SecAuthZ/security-descriptors)
</dt> <dt>

[Standard Zugriffsrechte](/windows/desktop/SecAuthZ/standard-access-rights)
</dt> <dt>

[Access Control Modell](/windows/desktop/SecAuthZ/access-control-model)
</dt> </dl>

 

 