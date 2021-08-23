---
title: Festlegen eines Zugriffssteuerungs-ACE in der Zugriffssteuerungsliste eines Objekts
description: Mit ADSI legen Sie einen ACE für den Zugriffssteuerungszugriff genau wie einen eigenschaftenspezifischen ACE fest, mit der Ausnahme, dass die IADsAccessControlEntry.ObjectType-Eigenschaft die rightsGUID des Steuerelementzugriffsrechtes ist.
ms.assetid: 454dc372-47b0-457d-8660-644fcfa59be8
ms.tgt_platform: multiple
keywords:
- Festlegen eines Zugriffssteuerungs-ACE in der Zugriffssteuerungsliste eines Objekts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09f4a4406bfa3d16a3e3be228bf4a0f131d77ad68cb99a6b9b2a8d328f15215e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024808"
---
# <a name="setting-a-control-access-right-ace-in-an-objects-acl"></a>Festlegen eines Zugriffssteuerungs-ACE in der Zugriffssteuerungsliste eines Objekts

Mit ADSI legen Sie einen ACE für den Zugriffssteuerungszugriff genau wie einen eigenschaftenspezifischen ACE fest, mit der Ausnahme, dass die [**IADsAccessControlEntry.ObjectType-Eigenschaft**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) die **rightsGUID** des Steuerelementzugriffsrechtes ist. Beachten Sie, dass Sie auch die Win32-Sicherheits-APIs verwenden können, um ACLs für Verzeichnisobjekte festzulegen.

In der folgenden Tabelle sind die [**IADsAccessControlEntry-Eigenschaften**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry) für Zugriffssteuerungsrechte aufgeführt, die zum Festlegen von Eigenschaften für einen ACE verwendet werden können.



| Eigenschaft                                                       | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Accessmask**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) | Für Zugriffssteuerungsrechte, die den Erweiterten Rechtezugriff auf spezielle Vorgänge steuern, muss AccessMask das **ADS \_ RIGHT \_ DS CONTROL \_ \_ ACCESS-Flag** enthalten. Für Zugriffssteuerungsrechte, die einen Eigenschaftensatz definieren, enthält AccessMask **ADS \_ RIGHT \_ DS READ \_ \_ PROP** und/oder **ADS RIGHT \_ \_ DS WRITE \_ \_ PROP**.<br/> Für Zugriffssteuerungsrechte, die überprüfte Schreibvorgänge steuern, enthält [**AccessMask**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) **ADS RIGHT \_ \_ DS \_ SELF**.<br/> |
| [**Flaggen**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods)      | Dieser Wert muss das **ADS FLAG OBJECT TYPE \_ \_ \_ \_ PRESENT-Flag** enthalten.                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**ObjektType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) | Dieser Wert muss das [**StringFromGUID2-Format**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2) des **rightsGUID-Attributs** des Zugriffssteuerungsrechts sein. Beachten Sie, dass die GUID-Zeichenfolge in einem ACE die startenden und abschließenden geschweiften Klammern enthalten muss, obwohl das **rightsGUID-Attribut** des **controlAccessRight-Objekts** die geschweiften Klammern nicht enthält.                                                                                                                                     |
| [**AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods)    | Entweder **ADS \_ ACETYPE ACCESS ALLOWED \_ \_ \_ OBJECT,** um dem Vertrauensnehmer das Zugriffssteuerungsrecht zu gewähren, oder **ADS \_ ACETYPE ACCESS \_ \_ DENIED \_ OBJECT,** um dem Vertrauensnehmer das Steuerelementzugriffsrecht zu verweigern.                                                                                                                                                                                                                                                                                                     |
| [**Treuhänder**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods)    | Der Sicherheitsprinzipal, z. B. Benutzer, Gruppe, Computer usw., für den der ACE gilt.                                                                                                                                                                                                                                                                                                                                                                                              |



 

Weitere Informationen zum Erstellen eines ACE finden Sie unter [Festlegen von Zugriffsrechten für ein Objekt.](setting-access-rights-on-an-object.md)

Weitere Informationen und ein Codebeispiel zum Festlegen eines ACE finden Sie unter [Beispielcode zum Festlegen eines ACE für ein Verzeichnisobjekt.](example-code-for-setting-an-ace-on-a-directory-object.md)

 

