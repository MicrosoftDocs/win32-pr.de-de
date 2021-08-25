---
title: Einrichten der Erweiterungs-DLLs
description: Beim Start überprüft NPS die Registrierung auf eine Liste der dlLs von Drittanbietern, die sie aufrufen können.
ms.assetid: fbbd9031-3ebe-47b8-8d8b-e359fa7d4b67
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 737d53bd25a28321c333e890a019af881ae54fa1c5ae92299b1776689f9abb74
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962510"
---
# <a name="setting-up-the-extension-dlls"></a>Einrichten der Erweiterungs-DLLs

> [!Note]  
> Internet Authentication Service (IAS) wurde ab Windows Server 2008 in Network Policy Server (NPS) umbenannt. Der Inhalt dieses Themas gilt sowohl für IAS als auch für NPS. Im gesamten Text wird NPS verwendet, um auf alle Versionen des Diensts zu verweisen, einschließlich der Versionen, die ursprünglich als IAS bezeichnet wurden.

 

Beim Start überprüft NPS die Registrierung auf eine Liste der dlLs von Drittanbietern, die sie aufrufen können.

Zum Einrichten einer Authentifizierungs- oder Autorisierungs-DLL auf einem NPS-Server listen Sie die Pfade zu den DLLs in Werten unter dem folgenden Registrierungsschlüssel auf:

**AuthSrv-Parameter des HKLM-Systems \\ \\ "CurrentControlSet \\ \\ \\ Services"\\**

Wenn die **Schlüssel AuthSrv** und **Parameters** nicht vorhanden sind, erstellen Sie sie.

Der Wert, in dem die Authentifizierungserweiterungs-DLLs aufgeführt werden, ist:

**ExtensionDLLs**

Der Wert, in dem die Autorisierungserweiterungs-DLLs aufgeführt werden, ist:

**AuthorizationDLLs**

Sowohl die **Werte ExtensionDLLs** als **auch AuthorizationDLLs** müssen vom Typ **REG MULTI SZ \_ \_ sein.** Mit diesem Typ können Sie mehrere DLLs auflisten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aufrufen der Erweiterungs-DLLs](/windows/desktop/Nps/ias-authentication-and-authorization-process)
</dt> <dt>

[Benutzeridentifikationsattribute](/windows/desktop/Nps/ias-user-identification-attributes)
</dt> </dl>

 

 