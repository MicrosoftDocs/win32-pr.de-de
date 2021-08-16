---
description: 'Die Xenroll.dll bibliothek enthält die folgenden Methoden und Eigenschaften, die Sie zum Verwalten von Zertifikatspeichern verwenden können. FunctionsDescriptionCAStoreFlagsSpecifis or returns flags that control access to the certification authority (CA) store. CAStoreNameWStrS gibt den Namen des Zertifizierungsstellenspeichers an oder gibt den Namen zurück. CAStoreTypeWStrS gibt den Typ des Speichers an, der durch die CAStoreName-Eigenschaft identifiziert wird, oder gibt diesen zurück. MyStoreFlagsSpecifis or returns a flag that determines the path of the personal store. MyStoreNameWStrS gibt den Namen des persönlichen Speichers an oder gibt den Namen zurück. MyStoreTypeWStrS gibt den Typ des persönlichen Speichers an oder gibt diesen zurück. RequestStoreFlags Gibt ein Flag an, das den Pfad des Anforderungsspeichers bestimmt, oder gibt dieses zurück. RequestStoreNameWStrS gibt den Namen des Anforderungsspeichers an oder gibt den Namen zurück. RequestStoreTypeWStrS gibt den Typ des Anforderungsspeichers an oder gibt diesen zurück. RootStoreFlagsSpecifis or returns a flag that determines the path of the root store. RootStoreNameWStrS gibt den Namen des Stammspeichers an oder gibt den Namen zurück. RootStoreTypeWStrS gibt den Typ des Stammspeichers an oder gibt diesen zurück. SetHStoreCAS gibt das Handle des ZS-Speichers an. SetHStoreMySpecs gibt das Handle des persönlichen Speichers an. SetHStoreRequest Gibt das Handle des Anforderungsspeichers an. SetHStoreROOT Gibt das Handle des Stammspeichers an. '
ms.assetid: 15e4368b-4199-415a-9c2c-2c1351b717e6
title: Certificate Store Functions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53a90a6fd2146517d4d70f653da42961274301a3058f8dbad9e72b8b90228bc1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118902174"
---
# <a name="certificate-store-functions"></a>Certificate Store Functions

Die Xenroll.dll bibliothek enthält die folgenden Methoden und Eigenschaften, die Sie zum Verwalten von Zertifikatspeichern verwenden können.

| Functions                                                          | BESCHREIBUNG                                                                                                                                                                                          |
|--------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CAStoreFlags**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_castoreflags)                 | Gibt Flags an oder gibt flags zurück, die den Zugriff auf [*den*](/windows/desktop/SecGloss/c-gly) Speicher der Zertifizierungsstelle steuern.<br/> |
| [**CAStoreNameWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_castorenamewstr)           | Gibt den Namen des Zertifizierungsstellenspeichers an oder gibt den Namen zurück.<br/>                                                                                                                                            |
| [**CAStoreTypeWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_castoretypewstr)           | Gibt den Typ des Speichers an, der durch die **CAStoreName-Eigenschaft identifiziert** wird, oder gibt diesen zurück.<br/>                                                                                                    |
| [**MyStoreFlags**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_mystoreflags)                 | Gibt ein Flag an oder gibt es zurück, das den Pfad des persönlichen Speichers bestimmt.<br/>                                                                                                               |
| [**MyStoreNameWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_mystorenamewstr)           | Gibt den Namen des persönlichen Speichers an oder gibt den Namen zurück.<br/>                                                                                                                                      |
| [**MyStoreTypeWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_mystoretypewstr)           | Gibt den Typ des persönlichen Speichers an oder gibt diesen zurück.<br/>                                                                                                                                      |
| [**RequestStoreFlags**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_requeststoreflags)       | Gibt ein Flag an, das den Pfad des Anforderungsspeichers bestimmt, oder gibt es zurück.<br/>                                                                                                                |
| [**RequestStoreNameWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_requeststorenamewstr) | Gibt den Namen des Anforderungsspeichers an oder gibt den Namen zurück.<br/>                                                                                                                                       |
| [**RequestStoreTypeWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_requeststoretypewstr) | Gibt den Typ des Anforderungsspeichers an oder gibt diesen zurück.<br/>                                                                                                                                       |
| [**RootStoreFlags**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_rootstoreflags)             | Gibt ein Flag an, das den Pfad des Stammspeichers bestimmt, oder gibt dieses zurück.<br/>                                                                                                                   |
| [**RootStoreNameWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_rootstorenamewstr)       | Gibt den Namen des Stammspeichers an oder gibt den Namen zurück.<br/>                                                                                                                                          |
| [**RootStoreTypeWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_rootstoretypewstr)       | Gibt den Typ des Stammspeichers an oder gibt diesen zurück.<br/>                                                                                                                                          |
| [**SetHStoreCA**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-sethstoreca)                   | Gibt das Handle des ZS-Speichers an.<br/>                                                                                                                                                     |
| [**SetHStoreMy**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-sethstoremy)                   | Gibt das Handle des persönlichen Speichers an.<br/>                                                                                                                                               |
| [**SetHStoreRequest**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-sethstorerequest)         | Gibt das Handle des Anforderungsspeichers an.<br/>                                                                                                                                                |
| [**SetHStoreROOT**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-sethstoreroot)               | Gibt das Handle des Stammspeichers an.<br/>                                                                                                                                                   |



 

CertEnroll.dll exportiert keine Funktionen, mit denen Sie Speichereigenschaftswerte angeben oder abrufen oder Zertifikate in bestimmte Speicher kopieren können.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zuordnen Xenroll.dll zu CertEnroll.dll](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> </dl>

 

