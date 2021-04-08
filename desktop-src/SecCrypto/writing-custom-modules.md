---
description: Sie können Richtlinien Module in der Programmiersprache C, C++ oder Visual Basic schreiben.
ms.assetid: 37a93c67-02f2-4c4e-a000-2bb98e0ca948
title: Schreiben von benutzerdefinierten Modulen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92247cd6b975bac520032dcc3aada1328f7b6c2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103959865"
---
# <a name="writing-custom-modules"></a>Schreiben von benutzerdefinierten Modulen

Sie können Richtlinien Module in der Programmiersprache C, C++ oder Visual Basic schreiben. Der erforderliche Microsoft-Compiler ist in Visual C++ Version 5,0 oder höher oder in Visual Basic Version 5,0 oder höher verfügbar. Eine Unternehmens [*Zertifizierungsstelle (Certification Authority*](../secgloss/c-gly.md) , ca) sollte nur das von Microsoft bereitgestellte Enterprise Policy-Modul verwenden.

Sie müssen [**icertpolicy**](/windows/desktop/api/Certpol/nn-certpol-icertpolicy) implementieren, wenn Sie ein benutzerdefiniertes Richtlinien Modul schreiben. Außerdem müssen Sie [**icertmanagemodule**](/windows/desktop/api/Certmod/nn-certmod-icertmanagemodule) implementieren, wenn Sie ein benutzerdefiniertes Richtlinien Modul schreiben.

Richtlinien Module können Methoden von [**icertserverpolicy**](/windows/desktop/api/Certif/nn-certif-icertserverpolicy) abrufen, um die Verarbeitung einer [*Zertifikat Anforderung*](../secgloss/c-gly.md)zu unterstützen. **Icertserverpolicy** ermöglicht das Festlegen und Abrufen von Eigenschaften und Zertifikat Erweiterungen.

Weitere Informationen finden Sie in den nachfolgenden Themen.



| Thema                                                                      | BESCHREIBUNG                             |
|----------------------------------------------------------------------------|-----------------------------------------|
| [Festlegen von Zertifikat Eigenschaften](setting-certificate-properties.md)       | Festlegen der Eigenschaften eines Zertifikats |
| [Schreiben von benutzerdefinierten Exit-Modulen](writing-custom-exit-modules.md)             | Schreiben von benutzerdefinierten Exit-Modulen             |
| [Schreiben von benutzerdefinierten Erweiterungs Handlern](writing-custom-extension-handlers.md) | Schreiben von benutzerdefinierten Erweiterungs Handlern       |



 

 

 
