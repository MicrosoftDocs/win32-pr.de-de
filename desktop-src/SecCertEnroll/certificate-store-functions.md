---
description: 'Die Xenroll.dll-Bibliothek enthält die folgenden Methoden und Eigenschaften, die Sie zum Verwalten von Zertifikat speichern verwenden können. Functionsdescriptioncastoreflagsgibt Flags an, die den Zugriff auf den Zertifizierungsstellen Speicher steuern, oder gibt diese zurück. Castorenamewstrauch gibt den Namen des ca-Stores an oder gibt diesen zurück. Castoretyetwstrauch gibt den Typ des durch die Eigenschaft "castorename" identifizierten Stores an oder gibt diesen zurück. Mystoreflagsgibt ein Flag an, das den Pfad des persönlichen Stores bestimmt, oder gibt es zurück. Mystorenamewstrauch gibt den Namen des persönlichen Stores an oder gibt diesen zurück. Mystoretypeer wstrauch gibt den Typ des persönlichen Stores an oder gibt diesen zurück. Requeststoreflagsgibt ein Flag an, das den Pfad des Anforderungs Speichers bestimmt, oder gibt es zurück. Requeststorenamewstrauch gibt den Namen des Anforderungs Speichers an oder gibt diesen zurück. Requeststoretypeer wstrauch gibt den Typ des Anforderungs Speichers an oder gibt diesen zurück. Rootstoreflagsgibt ein Flag an, das den Pfad des Stamm Speicher bestimmt, oder gibt es zurück. Rootstorenamewstrauch gibt den Namen des Stamm Speicher an oder gibt diesen zurück. Rootstoretypeer wstrauch gibt den Typ des Stamm Speicher an oder gibt diesen zurück. Das Handle des ca-Stores wird von "" von "". Das Handle des persönlichen Stores wird von "" durch "" festgelegt. Sethstorerequestgibt das Handle des Anforderungs Speichers an. "Tthstoreroot" gibt das Handle des Stamm Speicher an. '
ms.assetid: 15e4368b-4199-415a-9c2c-2c1351b717e6
title: Zertifikat Speicherfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d00ab4b7245f999e1131f41172b3c77af8b9c2aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350360"
---
# <a name="certificate-store-functions"></a>Zertifikat Speicherfunktionen

Die Xenroll.dll-Bibliothek enthält die folgenden Methoden und Eigenschaften, die Sie zum Verwalten von Zertifikat speichern verwenden können.

| Functions                                                          | BESCHREIBUNG                                                                                                                                                                                          |
|--------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Castoreflags**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_castoreflags)                 | Gibt Flags an, die den Zugriff auf den [*Zertifizierungs*](/windows/desktop/SecGloss/c-gly) stellen Speicher steuern, oder gibt diese zurück.<br/> |
| [**Castorenamewstr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_castorenamewstr)           | Gibt den Namen des ca-Stores an oder gibt diesen zurück.<br/>                                                                                                                                            |
| [**Castoretypeer WSTR**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_castoretypewstr)           | Gibt den Typ des durch die Eigenschaft " **castorename** " identifizierten Stores an oder gibt diesen zurück.<br/>                                                                                                    |
| [**MyStoreFlags**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_mystoreflags)                 | Gibt ein Flag an, das den Pfad des persönlichen Stores bestimmt, oder gibt es zurück.<br/>                                                                                                               |
| [**Mystorenamewstr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_mystorenamewstr)           | Gibt den Namen des persönlichen Stores an oder gibt diesen zurück.<br/>                                                                                                                                      |
| [**Mystoretypeer WSTR**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_mystoretypewstr)           | Gibt den Typ des persönlichen Stores an oder gibt diesen zurück.<br/>                                                                                                                                      |
| [**RequestStoreFlags**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_requeststoreflags)       | Gibt ein Flag an, das den Pfad des Anforderungs Speicher bestimmt, oder gibt es zurück.<br/>                                                                                                                |
| [**Requeststorenamewstr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_requeststorenamewstr) | Gibt den Namen des Anforderungs Speicher an oder gibt diesen zurück.<br/>                                                                                                                                       |
| [**Requeststoretypeer WSTR**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_requeststoretypewstr) | Gibt den Typ des Anforderungs Speicher an oder gibt diesen zurück.<br/>                                                                                                                                       |
| [**Rootstoreflags**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_rootstoreflags)             | Gibt ein Flag an, das den Pfad des Stamm Speicher bestimmt, oder gibt es zurück.<br/>                                                                                                                   |
| [**Rootstorenamewstr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_rootstorenamewstr)       | Gibt den Namen des Stamm Speicher an oder gibt diesen zurück.<br/>                                                                                                                                          |
| [**Rootstoretypeer WSTR**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_rootstoretypewstr)       | Gibt den Typ des Stamm Speicher an oder gibt diesen zurück.<br/>                                                                                                                                          |
| [**"Ziel"**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-sethstoreca)                   | Gibt das Handle des Zertifizierungsstellen Speicher an.<br/>                                                                                                                                                     |
| [**"Ab-storemy"**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-sethstoremy)                   | Gibt das Handle für den persönlichen Speicher an.<br/>                                                                                                                                               |
| [**"Tthstorerequest"**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-sethstorerequest)         | Gibt das Handle des Anforderungs Speicher an.<br/>                                                                                                                                                |
| [**"Ziel"**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-sethstoreroot)               | Gibt das Handle des Stamm Speicher an.<br/>                                                                                                                                                   |



 

CertEnroll.dll exportiert keine Funktionen, mit denen Sie Speicher Eigenschaftswerte angeben oder Abrufen oder Zertifikate in bestimmte Speicher kopieren können.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zuordnung von Xenroll.dll zu CertEnroll.dll](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> </dl>

 

