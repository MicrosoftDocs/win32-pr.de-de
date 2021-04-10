---
title: Aushandlung der Sicherheits Pauschale
description: Aushandlung der Sicherheits Pauschale
ms.assetid: 5a01912d-611c-4a6e-ab9d-0243cba331f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e51407de908eaaf0f79eea452046f8e424ccf900
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104039681"
---
# <a name="security-blanket-negotiation"></a>Aushandlung der Sicherheits Pauschale

Eine Sicherheits Pauschale ist eine Gruppe von Werten, die die Sicherheitseinstellungen beschreiben, die für alle Proxys in einem Prozess oder nur für einen bestimmten Schnittstellen Proxy gelten. Eine Sicherheits Pauschale besteht aus den folgenden Werten:

-   Authentifizierungsdienst
-   Autorisierungs Dienst
-   Prinzipalname
-   Authentifizierungs Ebene
-   Ebene des Identitätswechsels
-   Authentifizierungsidentität
-   Funktionen
-   Eine Zugriffs Steuerungs Liste (ACL) (nur Server)

Die sicherheitspauseaushandlung ist der Prozess, den com verwendet, um die Sicherheitseinstellungen für einen Proxy auszuwählen, wenn dieser erstellt wird. Dieser Prozess umfasst den Vergleich der Sicherheits übereindecke des Servers mit der Sicherheits Pauschale des Clients und die Verwendung dieser Werte, um eine entsprechende Standard Sicherheitsmetriken für den Proxy zu erstellen. In den folgenden Abschnitten wird erläutert, wo die Sicherheits decken des Clients und des Servers stammen, und es wird beschrieben, wie com die Sicherheits Pauschale für den Proxy mithilfe der Sicherheits decken des Clients und des Servers aushandiert.

Sowohl der Client als auch der Server können [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) abrufen, um die jeweiligen Sicherheits decken anzugeben. Wenn eine Anwendung **CoInitializeSecurity** nicht explizit aufruft, ruft com Sie implizit für die Anwendung auf, wobei die entsprechenden Standardwerte verwendet werden. Weitere Informationen zu diesen Standardwerten finden Sie unter [com-Sicherheits](com-security-defaults.md)Standards.

Einige Parameter für [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) gelten, wenn es sich bei der Anwendung um einen Server handelt, und einige gelten, wenn es sich bei der Anwendung um einen Client handelt. Wenn die Anwendung als Server fungiert, sind diese Parameter relevant: eine ACL, eine Liste mit Tupeln für den Authentifizierungsdienst/-Autorisierungs Dienst/-Prinzipal Namen und eine Authentifizierungs Ebene. Der **CoInitializeSecurity**-Rückruf eines Servers bestimmt, ob es sich um einen impliziten oder expliziten Wert handelt.

Wenn die Anwendung als Client fungiert, sind die folgenden Werte, die an [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) übermittelt werden, relevant: eine Authentifizierungs Ebene, eine Identitätswechsel Ebene, die Authentifizierungs Identität und Funktionen. Der implizite oder explizite **CoInitializeSecurity** -Rückruf eines Clients gibt die Sicherheits Pauschale an, die der Client wünscht.

Beim Erstellen eines Proxys verwendet com die Werte, die in der Sicherheits-und der Sicherheits Pauschale des Servers angegeben sind, um eine standardmäßige Sicherheits Pauschale auszuhandeln, die für den Proxy geeignet ist. COM wählt einen Authentifizierungsdienst aus, der sowohl auf dem Client als auch auf dem Server funktioniert. Der Autorisierungs Dienst und der Prinzipal Name werden für die Zusammenarbeit mit dem Authentifizierungsdienst ausgewählt. Für die Authentifizierungs Ebene wählt com den höheren der Authentifizierungs Ebenen aus, die vom Client und dem Server angegeben werden. Die Identitätswechsel Ebene und die von com ausgewählten Funktionen sind diejenigen, die vom Client festgelegt werden. Die Authentifizierungs Identität ist die, die vom Client für den ausgewählten Authentifizierungsdienst angegeben wird.

Nachdem die Standard Sicherheits Pauschale berechnet wurde, werden die zugehörigen Werte dem neu erstellten Proxy zugewiesen. Der Client kann die Sicherheitseinstellungen für den Proxy überschreiben, indem er [**IClientSecurity:: setblanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket)aufruft. Die für **setblanket** angegebenen Werte werden nicht ausgehandelt. Sie werden dem angegebenen Proxy einfach zugewiesen. Wenn jedoch Standardparameter (z. b. der Standardwert der RPC- \_ C- \_ \_ \_ Standard Ebene) an **setblanket** weitergegeben werden, verwendet com den zuvor beschriebenen Algorithmus für die sicherheitspauseaushandlung, um die Standardparameter zu berechnen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Sicherheit in com](security-in-com.md)
</dt> </dl>

 

 