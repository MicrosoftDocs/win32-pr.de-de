---
description: Die Tabelle AppId oder die Tabelle Registry gibt an, dass das Installationsprogramm DCOM-Server für einen der folgenden Schritte während einer Installation konfiguriert und registriert.
ms.assetid: d76ed6df-944b-4996-bf07-e42ceb7a1b69
title: AppId-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d9a121e6252c6054d5ac2765a9649e345035dde
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882219"
---
# <a name="appid-table"></a>AppId-Tabelle

Die Tabelle AppId oder [die Tabelle Registry](registry-table.md) gibt an, dass das Installationsprogramm DCOM-Server für einen der folgenden Schritte während einer Installation konfiguriert und registriert.

-   Führen Sie den DCOM-Server unter einer anderen Identität als der Benutzer aus, der den Server aktiviert. Zum Beispiel, um einen DCOM-Server so zu konfigurieren, dass er immer als interaktiver Benutzer oder als vordefinierter Benutzer ausgeführt wird.
-   Führen Sie den DCOM-Server als Dienst aus.
-   Konfigurieren Sie den Standardsicherheitszugriff für den DCOM-Server.
-   Registrieren Sie den DCOM-Server so, dass er auf einem anderen Computer aktiviert wird.

Diese Tabelle wird bei der Installation der Komponente verarbeitet, die dem DCOM-Server in der Spalte Komponente der \_ [Class-Tabelle zugeordnet ist.](class-table.md) Eine AppId wird nicht angekündigt.

Die AppId-Tabelle enthält die folgenden Spalten.



| Spalte               | Typ                       | Schlüssel | Nullwerte zulässig |
|----------------------|----------------------------|-----|----------|
| AppId                | [GUID](guid.md)           | J   | N        |
| RemoteServerName     | [Formatiert](formatted.md) | N   | J        |
| LocalService         | [Text](text.md)           | N   | J        |
| ServiceParameters    | [Text](text.md)           | N   | J        |
| DllSurrogate         | [Text](text.md)           | N   | J        |
| ActivateAtStorage    | [Integer](integer.md)     | N   | J        |
| RunAsInteractiveUser | [Integer](integer.md)     | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="AppId"></span><span id="appid"></span><span id="APPID"></span>Appid
</dt> <dd>

Die AppId-Spalte der [Tabelle Class ist](class-table.md) ein Fremdschlüssel in dieser Spalte der AppId-Tabelle. Diese Spalte enthält den AppId-Wert, der unter der CLSID geschrieben wird, und erstellt den AppId-GUID-Schlüssel unter HKCR \\ AppId.

</dd> <dt>

<span id="RemoteServerName"></span><span id="remoteservername"></span><span id="REMOTESERVERNAME"></span>RemoteServerName
</dt> <dd>

Diese Spalte enthält den Wert von "RemoteServerName"= xxxx, der &lt; &gt; unter HKCR \\ AppID \\ {AppID} geschrieben \\ wird.

</dd> <dt>

<span id="LocalService"></span><span id="localservice"></span><span id="LOCALSERVICE"></span>Localservice
</dt> <dd>

Diese Spalte enthält den Wert von LocalService, der unter HKCR \\ AppID \\ { &lt; appid &gt; } "LocalService"= &lt; xxx geschrieben &gt; wird.

</dd> <dt>

<span id="ServiceParameters"></span><span id="serviceparameters"></span><span id="SERVICEPARAMETERS"></span>ServiceParameters
</dt> <dd>

Diese Spalte enthält den Wert von ServiceParameters, der unter HKCR \\ AppID \\ {appid>} "ServiceParameters" geschrieben wird.

</dd> <dt>

<span id="DllSurrogate"></span><span id="dllsurrogate"></span><span id="DLLSURROGATE"></span>DllSurrogate
</dt> <dd>

Diese Spalte enthält den Wert von DllSurrogate, der unter HKCR \\ AppId \\ { &lt; appid &gt; } "DllSurrogate"= &lt; xxx geschrieben &gt; wird. Wenn diese Spalte vorhanden ist, handelt es sich in der Regel um eine leere Zeichenfolge.

</dd> <dt>

<span id="ActivateAtStorage"></span><span id="activateatstorage"></span><span id="ACTIVATEATSTORAGE"></span>ActivateAtStorage
</dt> <dd>

Ein ganzzahliger Wert, der nicht 0 (null) in diesem Feld ist, bewirkt, dass Windows Installer HKCR \\ AppID \\ { &lt; appid &gt; } "ActivateAtStorage"="Y" in die Registrierung schreibt. Wenn das Feld leer gelassen wird oder den Wert 0 hat, wird kein Wert geschrieben.

</dd> <dt>

<span id="RunAsInteractiveUser"></span><span id="runasinteractiveuser"></span><span id="RUNASINTERACTIVEUSER"></span>RunAsInteractiveUser
</dt> <dd>

Ein ganzzahliger Wert, der nicht 0 (null) in diesem Feld ist, bewirkt, dass Windows Installer HKCR \\ AppID \\ {appid>} "RunAs"="Interactive User" in die Registrierung schreibt. Wenn das Feld leer gelassen wird oder den Wert 0 hat, wird kein Wert geschrieben.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Tabelle wird von der [Aktion RegisterClassInfo und](registerclassinfo-action.md) der [UnregisterClassInfo-Aktion verwendet.](unregisterclassinfo-action.md)

Beachten Sie, dass die AppId-Tabelle keine Spalte zum Registrieren eines Standardnamens enthält. Daher müssen Sie sich in Fällen, in denen Sie einen Benutzeroberflächennamen als Standardwert schreiben müssen, mithilfe der [Registrierungstabelle registrieren.](registry-table.md)

## <a name="validation"></a>Validierung

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE33](ice33.md)  
[ICE46](ice46.md)  
[ICE69](ice69.md)  
</dl>

 

 



