---
description: Zum Erstellen einer Sicherheits Beschreibung kann ein geschützter Server dieselbe Prozedur verwenden, die von einer Anwendung verwendet wird, um eine Sicherheits Beschreibung für ein Sicherungs fähiges Objekt zu erstellen.
ms.assetid: f40c4b62-a3f0-4e66-875e-2ef904d052e5
title: Sicherheits Deskriptoren für private Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97c40dc5c4e9f0a3d0e641874153d2862d038a19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959065"
---
# <a name="security-descriptors-for-private-objects"></a>Sicherheits Deskriptoren für private Objekte

Zum Erstellen einer [*Sicherheits Beschreibung*](/windows/desktop/SecGloss/s-gly)kann ein geschützter Server dieselbe Prozedur verwenden, die von einer Anwendung verwendet wird, um eine Sicherheits Beschreibung für ein Sicherungs fähiges Objekt zu erstellen. Beispielcode finden Sie unter [Erstellen einer Sicherheits Beschreibung für ein neues Objekt in C++](creating-a-security-descriptor-for-a-new-object-in-c--.md). Alternativ kann eine geschützte Serveranwendung die [**buildsecuritydescriptor**](/windows/desktop/api/Aclapi/nf-aclapi-buildsecuritydescriptora) -Funktion für dies ausführen. Wenn ein Zeiger auf eine vorhandene [*selbst relative Sicherheits Beschreibung*](/windows/desktop/SecGloss/s-gly) für **buildsecuritydescriptor** bereitgestellt wird, erstellt er die neue Sicherheits Beschreibung mit Informationen, die von dieser Sicherheits Beschreibung erstellt werden, die mit neuen Access Control-Informationen zusammengeführt wird, die im Funktions aufrufals Parameter übergeben wurden. Der Besitzer und die Gruppe werden optional durch Vertrauens nehmer-Strukturen angegeben, die an die [**Funktion übermittelt**](/windows/desktop/api/AccCtrl/ns-accctrl-trustee_a) werden. Die von **buildsecuritydescriptor** erstellte Sicherheits Beschreibung ist in einem *selbst relativen* Format enthalten.

Außerdem bietet die Windows-API eine Reihe von Funktionen zum Zusammenführen von Client Sicherheitsinformationen mit Informationen, die von der Sicherheits Beschreibung für ein übergeordnetes Objekt oder von einer Standard Sicherheits Beschreibung geerbt wurden. Die Funktionen " [**kreateprivateobjectsecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-createprivateobjectsecurity)", " [**GetPrivateObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getprivateobjectsecurity)", " [**setprivateobjectsecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setprivateobjectsecurity)" und " [**DestroyPrivateObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-destroyprivateobjectsecurity) " bieten die Möglichkeit, Standardinformationen von einem [*Zugriffs Token*](/windows/desktop/SecGloss/a-gly)abzurufen, Vererbung zu unterstützen und bestimmte Teile der Sicherheits Beschreibung zu bearbeiten. Dies kann hilfreich sein, wenn ein Client ein privates Objekt in einer Hierarchie von gesicherten Objekten erstellt. Sie können z. b. mit **der Funktion** "" von "" die Funktion "" von "" die Funktion "" in der Sicherheits Beschreibung erstellen, die vom Client angegebene ACEs, von einem übergeordneten Objekt geerbte ACEs und den Standard Besitzer aus dem Erstellungs Client-Zugriffs Token enthält. Während von [**buildsecuritydescriptor**](/windows/desktop/api/Aclapi/nf-aclapi-buildsecuritydescriptora) Sicherheits Deskriptoren aus Zugriffs Steuerungsinformationen erstellt werden, die an den Funktions-oder eine vorhandene Sicherheits Beschreibung übergeben werden, erstellt " **kreateprivateobjectsecurity** " eine Sicherheits Beschreibung, die ausschließlich aus den Informationen in vorhandenen Sicherheits Beschreibungen besteht.

Die [**lookupsecuritydescriptorparts**](/windows/desktop/api/Aclapi/nf-aclapi-lookupsecuritydescriptorpartsa) -Funktion ruft Sicherheits Deskriptorinformationen aus einer vorhandenen [*selbst relativen Sicherheits Beschreibung*](/windows/desktop/SecGloss/s-gly)ab. Diese Informationen umfassen die Besitzer-und Gruppen Spezifikation, die Anzahl der ACEs in der SACL oder DACL und die Liste der ACEs in der SACL oder DACL.

 

 
