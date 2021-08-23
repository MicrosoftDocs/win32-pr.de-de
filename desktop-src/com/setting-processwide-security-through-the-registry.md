---
title: Festlegen Process-Wide Sicherheit über die Registrierung
description: Wenn Sie die Sicherheit für einen gesamten Prozess festlegen möchten, besteht eine Lösung darin, die Gewünschten Sicherheitsebenen in der Registrierung festzulegen.
ms.assetid: 87f0a64f-f3ec-4ee2-8d65-4f82e8971f0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc8ad3a549a78a10b15e965ba2e2a47b9e5e84f1e8790ccfbf90af622051714e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119730910"
---
# <a name="setting-process-wide-security-through-the-registry"></a>Festlegen Process-Wide Sicherheit über die Registrierung

Wenn Sie die Sicherheit für einen gesamten Prozess festlegen möchten, besteht eine Lösung darin, die Gewünschten Sicherheitsebenen in der Registrierung festzulegen. Wenn Ihre Anwendung [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) nicht aufrufen kann oder wenn Sie keine programmgesteuerte Sicherheit verwenden möchten, ist dies möglicherweise eine gute Option. Wenn Sie die prozessweite Sicherheit mithilfe der Registrierung festlegen möchten, sollten Sie beachten, dass COM beim Aufrufen von **CoInitializeSecurity** in Ihrem Programm die Werte in **CoInitializeSecurity** verwendet und die Registrierungswerte ignoriert.

Es gibt zwei Möglichkeiten, die Sicherheit in der Registrierung für Ihre Anwendung festzulegen:

-   Sie können Dcomcnfg.exe verwenden, die eine einfache Benutzeroberfläche zum Ändern von Sicherheitswerten bereitstellt. Alle COM-Server können mit Dcomcnfg.exe konfiguriert werden. Weitere Informationen finden Sie unter [Setting Process-Wide Security Using DCOMCNFG](setting-processwide-security-using-dcomcnfg.md). Clientanwendungen werden jedoch normalerweise nicht in Dcomcnfg.exe angezeigt, es sei denn, der Client erstellt eine GUID und gibt sie in die Registrierung ein.
-   Sie können Sicherheitswerte unter dem [AppID-Schlüssel](appid-key.md) für die Anwendung festlegen. Im weiteren Verlauf dieses Themas wird erläutert, wie Sie die Sicherheit in der Registrierung mithilfe des **AppID-Schlüssels** festlegen.

Eine AppID ist eine GUID, die einen Serverprozess für eine oder mehrere Klassen darstellt. Jede Klasse ist genau einer AppID zugeordnet, und AppIDs können nur EXEs zugewiesen werden. DLLs erhalten appIDs nur dann, wenn sie in einem Ersatzzeichen ausgeführt werden, und dann ist es der Ersatzprozess, der über die AppID verfügt. Wenn mehrere DLLs in ein Ersatzzeichen geladen werden, verfügt jedes Ersatzzeichen nur über eine AppID.

Bei einigen COM-Servern generiert der Registrierungscode eine AppID und platziert Einträge in der Registrierung, die die AppID dem Namen der ausführbaren Datei zuordnen. Einige COM-Server bieten diese Funktionalität jedoch nicht. Wenn der Registrierungscode des Servers jedoch einen Eintrag für HKCR \\ CLSID{ServerCLSID} \\ [LocalServer32](localserver32.md) hinzufügt, wenn dcomcnfg.exe ausgeführt wird, wird automatisch eine AppID für die CLSID hinzugefügt.

Für einen COM-Client, der kein Server ist, wird diese Zuordnung nicht erstellt, da der Client nie registriert ist. Daher muss der Client die erforderlichen Registrierungseinträge entweder programmgesteuert mithilfe der [Registrierungsfunktionen](/windows/desktop/SysInfo/registry-functions) oder mit regedit erstellen, um die Sicherheit mithilfe des **AppID-Schlüssels** festzulegen.

Wenn Sie die prozessweite Sicherheit in der Registrierung unter dem **AppID-Schlüssel** festlegen möchten, beachten Sie, dass unter dem **AppID-Schlüssel** zwei benannte Werte vorhanden sind, die Sie ohne Administratorberechtigungen festlegen können:

-   [AccessPermission](accesspermission.md)
-   [Authenticationlevel](authenticationlevel.md)

Die Werte **AuthenticationLevel** und **AccessPermission** werden unabhängig voneinander festgelegt und weisen separate Standardwerte auf. Wenn der **AuthenticationLevel-Wert** nicht vorhanden ist, wird der [LegacyAuthenticationLevel-Wert](legacyauthenticationlevel.md) als Standardwert verwendet. Wenn der **AccessPermission-Wert** nicht vorhanden ist, wird der [DefaultAccessPermission-Wert](defaultaccesspermission.md) als Standardwert verwendet. Die Werte **AuthenticationLevel** und **AccessPermission** sind jedoch wie folgt miteinander verknüpft:

-   Wenn **AuthenticationLevel** kein Wert ist, werden die Werte **AccessPermission** und **DefaultAccessPermission** für diese Anwendung ignoriert.
-   Wenn **AuthenticationLevel** nicht vorhanden ist und **LegacyAuthenticationLevel** keine ist, werden die Werte **AccessPermission** und **DefaultAccessPermission** für diese Anwendung ignoriert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Festlegen von Process-Wide Security](setting-processwide-security.md)
</dt> </dl>

 

 