---
title: Einrichten der Erweiterungs-DLLs
description: Beim Start überprüft NPS die Registrierung auf eine Liste der aufzurufenden DLLs von Drittanbietern.
ms.assetid: fbbd9031-3ebe-47b8-8d8b-e359fa7d4b67
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14e8589f31144f12b120f9a77f281dd57a9f30ce
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039309"
---
# <a name="setting-up-the-extension-dlls"></a>Einrichten der Erweiterungs-DLLs

> [!Note]  
> Der Internet Authentifizierungsdienst (IAS) wurde ab Windows Server 2008 in den Netzwerk Richtlinien Server (Network Policy Server, NPS) umbenannt. Der Inhalt dieses Themas gilt sowohl für IAS als auch für NPS. Im gesamten Text wird NPS verwendet, um auf alle Versionen des Dienstanbieter zu verweisen, einschließlich der Versionen, die ursprünglich als IAS bezeichnet wurden.

 

Beim Start überprüft NPS die Registrierung auf eine Liste der aufzurufenden DLLs von Drittanbietern.

Wenn Sie eine Authentifizierungs-oder Autorisierungs-dll auf einem NPS-Server einrichten möchten, können Sie die Pfade zu den DLLs in Werten unter dem folgenden Registrierungsschlüssel auflisten:

**"HKLM \\ System \\ CurrentControlSet \\ Services \\ authsrv \\ Parameters"\\**

Wenn die Parameter " **authsrv** " und " **Parameters** " nicht vorhanden sind, erstellen Sie Sie.

Der Wert zum Auflisten der authentifizierungserweiterungs-DLLs lautet:

**Extensiondlls**

Der Wert für die Liste der Autorisierungs Erweiterungs-DLLs lautet:

**Authorizationdlls**

Die Werte für " **extensiondlls** " und " **authorizationdlls** " müssen den Typ " **reg \_ \_ MultiSZ**" aufweisen. Mit diesem Typ können Sie mehrere DLLs auflisten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aufrufen der Erweiterungs-DLLs](/windows/desktop/Nps/ias-authentication-and-authorization-process)
</dt> <dt>

[Benutzer Identifizierungs Attribute](/windows/desktop/Nps/ias-user-identification-attributes)
</dt> </dl>

 

 