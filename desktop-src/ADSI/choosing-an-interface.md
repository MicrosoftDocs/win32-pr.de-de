---
title: Auswählen einer Schnittstelle für die Bindung
description: Wenn ein Verzeichnisobjekt an gebunden ist, gibt der Aufrufer den gewünschten AdsI-Schnittstellentyp an.
ms.assetid: 3c86e136-6d82-4baf-9c76-27dac8ad68ac
ms.tgt_platform: multiple
keywords:
- ADSI ADSI , mithilfe von , Auswählen einer Schnittstelle für die Bindung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15dfb1f39a24f6113796ed81d5a3269cfc2134d8d68546170049dd2f8a70bb0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118180294"
---
# <a name="choosing-an-interface-for-binding"></a>Auswählen einer Schnittstelle für die Bindung

Wenn ein Verzeichnisobjekt an gebunden ist, gibt der Aufrufer den gewünschten AdsI-Schnittstellentyp an. Alle ADSI-Verzeichnisobjekte unterstützen die [**IADs-Schnittstelle.**](/windows/desktop/api/Iads/nn-iads-iads) Ein ADSI-Objekt kann auch andere Schnittstellen unterstützen. Die tatsächlichen Schnittstellen, die vom -Objekt unterstützt werden, hängen von der Objektklasse ab. Beispielsweise unterstützt ein Benutzerobjekt die [**IADsUser-Schnittstelle,**](/windows/desktop/api/Iads/nn-iads-iadsuser) aber nicht die [**IADsComputer-Schnittstelle.**](/windows/desktop/api/Iads/nn-iads-iadscomputer)

Automatisierungsclients sollten die Schnittstellen **IADs \** _ verwenden, da es sich bei diesen Schnittstellen um duale Schnittstellen handelt, die ein höheres Maß an Abstraktion bereitstellen und Daten mithilfe des [*_VARIANT-Datentyps* *](/windows/win32/api/oaidl/ns-oaidl-variant) bereitstellen.

Zusätzlich zu den Schnittstellen **IADs \** _ können C/C++-Clients die [Schnittstellen _ *IDirectoryObject* *](/windows/desktop/api/Iads/nn-iads-idirectoryobject) und [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) verwenden. Diese Schnittstellen sind keine dualen Schnittstellen und unterstützen keine Automatisierung. Diese Schnittstellen bieten eine bessere Kontrolle über genau die Attribute, die abgerufen werden sollen, und ermöglichen den Zugriff auf die in einer Eigenschaft gespeicherten Rohdaten. Wenn beispielsweise die [**IADs::Get-Methode**](/windows/desktop/api/Iads/nf-iads-iads-get) zum Abrufen des **ntSecurityDescriptor-Attributs** für ein Objekt verwendet wird, stellt die **IADs::Get-Methode** einen [**IDispatch-Schnittstellenzeiger**](/windows/win32/api/oaidl/nn-oaidl-idispatch) bereit, der die [**IADsSecurityDescriptor-Schnittstelle**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor) unterstützt. Die **IADsSecurityDescriptor-Schnittstelle** wird von ADSI bereitgestellt, um einen Sicherheitsdeskriptor zu darstellen. Wenn dagegen die [**IDirectoryObject::GetObjectAttributes-Methode**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) zum Abrufen des **ntSecurityDescriptor-Attributs** verwendet wird, stellt **IDirectoryObject::GetObjectAttributes** ein Bytearray zur Auswahl, das in eine [**SECURITY \_ DESCRIPTOR-Struktur**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) umgestellt werden kann. Die Win32-Sicherheits-APIs können mit diesen Daten verwendet werden, um den Sicherheitsdeskriptor zu bearbeiten.

 

 