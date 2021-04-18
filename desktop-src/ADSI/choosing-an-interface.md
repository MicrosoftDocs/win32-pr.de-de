---
title: Auswählen einer Schnittstelle für die Bindung
description: Wenn ein Verzeichnis Objekt an gebunden ist, gibt der Aufrufer den gewünschten Typ der ADSI-Schnittstelle an.
ms.assetid: 3c86e136-6d82-4baf-9c76-27dac8ad68ac
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, using, eine Schnittstelle für die Bindung auswählen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 444bd41d1567849d5bf3a85ac3ec22f317ced5d3
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104391006"
---
# <a name="choosing-an-interface-for-binding"></a>Auswählen einer Schnittstelle für die Bindung

Wenn ein Verzeichnis Objekt an gebunden ist, gibt der Aufrufer den gewünschten Typ der ADSI-Schnittstelle an. Alle ADSI-Verzeichnisobjekte unterstützen die [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) -Schnittstelle. Ein ADSI-Objekt kann auch andere Schnittstellen unterstützen. Die tatsächlich vom-Objekt unterstützten Schnittstellen sind von der-Klasse des-Objekts abhängig. Ein Benutzerobjekt unterstützt z. b. die [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) -Schnittstelle, unterstützt jedoch nicht die [**iadscomputer**](/windows/desktop/api/Iads/nn-iads-iadscomputer) -Schnittstelle.

Automatisierungs Clients sollten die **IADs \*** -Schnittstellen verwenden, da es sich bei diesen Schnittstellen um duale Schnittstellen handelt, die eine höhere Abstraktions Ebene bieten und Daten mit dem [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) -Datentyp bereitstellen

Zusätzlich zu den **\* IADs** -Schnittstellen können C/C++-Clients die [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) -Schnittstelle und die [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) -Schnittstelle verwenden. Diese Schnittstellen sind keine Dual Schnittstellen und unterstützen keine Automatisierung. Diese Schnittstellen bieten eine bessere Kontrolle darüber, welche Attribute abgerufen werden und wie der Zugriff auf die in einer Eigenschaft gespeicherten Rohdaten ermöglicht wird. Wenn z. b. die [**IADs:: Get**](/windows/desktop/api/Iads/nf-iads-iads-get) -Methode zum Abrufen des **ntSecurityDescriptor** -Attributs für ein Objekt verwendet wird, stellt die **IADs:: Get** -Methode einen [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstellen Zeiger bereit, der die [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor) -Schnittstelle unterstützt. Die **IADsSecurityDescriptor** -Schnittstelle wird von ADSI zur Darstellung einer Sicherheits Beschreibung bereitgestellt. Wenn die [**IDirectoryObject:: getobjectattributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) -Methode zum Abrufen des **ntSecurityDescriptor** -Attributs verwendet wird, stellt **IDirectoryObject:: getobjectattributes** im Vergleich ein Bytearray bereit, das in eine [**Sicherheits \_ deskriptorstruktur**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) umgewandelt werden kann. Die Win32-Sicherheits-APIs können mit diesen Daten verwendet werden, um die Sicherheits Beschreibung zu bearbeiten.

 

 