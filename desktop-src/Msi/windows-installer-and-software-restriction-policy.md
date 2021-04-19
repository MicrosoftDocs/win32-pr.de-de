---
description: Windows Installer ist in die Software Einschränkungs Richtlinie in Microsoft Windows XP integriert.
ms.assetid: b1e58336-8908-45ee-86f0-81b2314fa77a
title: Windows Installer-und Software Einschränkungs Richtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b080a1ed9a1396f4ac212e73d1fda6e2719bf40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363560"
---
# <a name="windows-installer-and-software-restriction-policy"></a>Windows Installer-und Software Einschränkungs Richtlinie

Windows Installer ist in die Software Einschränkungs Richtlinie in Microsoft Windows XP integriert. Die Software Einschränkungs Richtlinie kann über Gruppenrichtlinien konfiguriert werden. Die Software Einschränkungs Richtlinie ermöglicht es Administratoren, Administratoren und nicht Administratoren das Ausführen von Dateien auf der Grundlage der Pfad-, URL-Zonen-, Hash-oder Herausgeber Kriterien einzuschränken. Die Richtlinie für Software Einschränkung hat zwei Ebenen: uneingeschränkt und unzulässig. Mit der Windows Installer werden nur Pakete installiert, die auf uneingeschränkter Ebene ausgeführt werden dürfen.

Patches oder Transformationen müssen auch auf uneingeschränkter Ebene ausgeführt werden dürfen. Wenn ein Paket, ein Patch oder eine Transformation so konfiguriert ist, dass es auf einer anderen Ebene als uneingeschränkt ausgeführt wird, zeigt der Windows Installer eine Fehlermeldung an und protokolliert einen Eintrag im Anwendungs Ereignisprotokoll. Die Software Einschränkungs Richtlinie wird ausgewertet, wenn eine Anwendung zum ersten Mal installiert wird, wenn ein neuer Patch angewendet wird und wenn das Installationspaket erneut zwischengespeichert wird.

Wenn ein Paket, ein Patch oder eine Transformation eingeschränkt ist, zeigt der Windows Installer eine Fehlermeldung an und schreibt einen Eintrag für die [Ereignisprotokollierung](event-logging.md) in das Anwendungs Ereignisprotokoll. Die Software Einschränkungs Richtlinie wird ausgewertet, wenn eine Anwendung zum ersten Mal installiert wird, wenn ein neuer Patch angewendet wird und wenn das Installationspaket erneut zwischengespeichert wird.

Weitere Informationen zu Software Einschränkungs Richtlinien finden Sie in der Produktdokumentation und [Durchsuchen der TechNet-Website](https://www.microsoft.com/technet/sitemap.mspx).

 

 



