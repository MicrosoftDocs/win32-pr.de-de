---
title: Festlegen der Process-Wide Sicherheit über die Registrierung
description: Wenn Sie die Sicherheit für einen gesamten Prozess festlegen möchten, besteht eine Lösung darin, die in der Registrierung gewünschten Sicherheitsstufen festzulegen.
ms.assetid: 87f0a64f-f3ec-4ee2-8d65-4f82e8971f0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d303f184229cb20aef1cbf71733956a3b6ce6618
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103949150"
---
# <a name="setting-process-wide-security-through-the-registry"></a>Festlegen der Process-Wide Sicherheit über die Registrierung

Wenn Sie die Sicherheit für einen gesamten Prozess festlegen möchten, besteht eine Lösung darin, die in der Registrierung gewünschten Sicherheitsstufen festzulegen. Wenn Ihre Anwendung nicht [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) aufgerufen werden kann oder wenn Sie nicht die programmgesteuerte Sicherheit verwenden möchten, ist dies möglicherweise eine gute Option. Wenn Sie die Prozess weite Sicherheit mithilfe der Registrierung festlegen möchten, sollten Sie beachten, dass beim **CoInitializeSecurity** -Befehl im Programm com die Werte in **CoInitializeSecurity** verwendet und die Registrierungs Werte ignoriert werden.

Es gibt zwei Möglichkeiten, die Sicherheit in der Registrierung für Ihre Anwendung festzulegen:

-   Sie können Dcomcnfg.exe verwenden, das eine einfache Benutzeroberfläche zum Ändern von Sicherheits Werten bereitstellt. Alle com-Server können mithilfe von Dcomcnfg.exe konfiguriert werden. Weitere Informationen finden Sie unter [Festlegen von Process-Wide Sicherheit mithilfe von DCOMCNFG](setting-processwide-security-using-dcomcnfg.md). Client Anwendungen werden jedoch normalerweise nicht in Dcomcnfg.exe angezeigt, es sei denn, der Client erstellt eine GUID und gibt Sie in der Registrierung ein.
-   Sie können Sicherheitswerte unter dem [AppID](appid-key.md) -Schlüssel für die Anwendung festlegen. Im weiteren Verlauf dieses Themas wird erläutert, wie die Sicherheit mithilfe des **AppID** -Schlüssels in der Registrierung festgelegt wird.

Eine AppID ist eine GUID, die einen Server Prozess für eine oder mehrere Klassen darstellt. Jede Klasse ist genau einer AppID zugeordnet, und AppIDs können nur EXEs zugewiesen werden. DLLs erhalten keine APPIDs, es sei denn, Sie werden in einem Ersatzprogramm ausgeführt, und dann handelt es sich um den Ersatzprozess, der über die AppID verfügt. Wenn mehrere DLLs in ein Ersatz Zeichen geladen werden, verfügt jedes Ersatz Zeichen nur über eine AppID.

Bei einigen com-Servern generiert der Registrierungscode eine AppID und platziert Einträge in der Registrierung, die die AppID dem Namen der ausführbaren Datei zuordnen. Einige com-Server bieten diese Funktionalität jedoch nicht. Wenn der Registrierungscode des Servers jedoch einen Eintrag für HKCR \\ CLSID {serverclsid} \\ [LocalServer32](localserver32.md) hinzufügt, wenn dcomcnfg.exe ausgeführt wird, wird automatisch eine AppID für die CLSID hinzugefügt.

Bei einem com-Client, bei dem es sich nicht um einen Server handelt, wird diese Zuordnung nicht erstellt, da der Client nie registriert wird. Damit die Sicherheit mithilfe des **AppID** -Schlüssels festgelegt werden kann, muss der Client die erforderlichen Registrierungseinträge erstellen, entweder Programm gesteuert mithilfe der [Registrierungsfunktionen](/windows/desktop/SysInfo/registry-functions) oder mithilfe von regedit.

Wenn Sie die Prozess weite Sicherheit in der Registrierung unter dem Schlüssel " **AppID** " festlegen möchten, beachten Sie, dass es zwei benannte Werte unter dem Schlüssel " **AppID** " gibt, die Sie ohne Administrator Berechtigungen festlegen können:

-   [Access spermission](accesspermission.md)
-   [AuthenticationLevel](authenticationlevel.md)

Die Werte **AuthenticationLevel** und **AccessPermission** werden unabhängig voneinander festgelegt und verfügen über separate Standardwerte. Wenn der **AuthenticationLevel** -Wert nicht vorhanden ist, wird der [legacyauthenticationlevel](legacyauthenticationlevel.md) -Wert als Standardwert verwendet. Entsprechend wird der Wert [DefaultAccessPermission](defaultaccesspermission.md) als Standardwert verwendet, wenn der **AccessPermission** -Wert nicht vorhanden ist. Allerdings sind die Werte **AuthenticationLevel** und **AccessPermission** auf folgende Weise miteinander verknüpft:

-   Wenn **AuthenticationLevel** den Wert None hat, werden die Werte **AccessPermission** und **DefaultAccessPermission** für diese Anwendung ignoriert.
-   Wenn " **AuthenticationLevel** " nicht vorhanden ist und " **legacyauthenticationlevel** " auf "None" festgelegt ist, werden die Werte **AccessPermission** und **DefaultAccessPermission** für diese Anwendung ignoriert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Festlegen Process-Wide Sicherheit](setting-processwide-security.md)
</dt> </dl>

 

 