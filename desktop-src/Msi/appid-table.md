---
description: Die Tabelle AppId oder die Registrierungstabelle gibt an, dass das Installationsprogramm DCOM-Server für einen der folgenden Schritte während einer Installation konfiguriert und registriert.
ms.assetid: d76ed6df-944b-4996-bf07-e42ceb7a1b69
title: AppId-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e8452635cd7c167d6a8618629eaec2f6f6c1aa2e72e0b3628a7d4542a9e7160
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066270"
---
# <a name="appid-table"></a>AppId-Tabelle

Die Tabelle AppId oder die [Registrierungstabelle](registry-table.md) gibt an, dass das Installationsprogramm DCOM-Server für einen der folgenden Schritte während einer Installation konfiguriert und registriert.

-   Führen Sie den DCOM-Server unter einer anderen Identität als der Benutzer aus, der den Server aktiviert. Beispielsweise, um einen DCOM-Server so zu konfigurieren, dass er immer als interaktiver Benutzer oder als vordefinierter Benutzer ausgeführt wird.
-   Führen Sie den DCOM-Server als Dienst aus.
-   Konfigurieren Sie den Standardsicherheitszugriff für den DCOM-Server.
-   Registrieren Sie den DCOM-Server so, dass er auf einem anderen Computer aktiviert ist.

Diese Tabelle wird bei der Installation der Komponente verarbeitet, die dem DCOM-Server in der \_ Spalte Komponente der [Class-Tabelle](class-table.md)zugeordnet ist. Eine AppId wird nicht angekündigt.

Die Tabelle AppId enthält die folgenden Spalten.



| Spalte               | Typ                       | Key | Nullwerte zulässig |
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

Die AppId-Spalte der [Class-Tabelle](class-table.md) ist ein Fremdschlüssel in dieser Spalte der AppId-Tabelle. Diese Spalte enthält den AppId-Wert, der unter der CLSID geschrieben wird, und erstellt den AppId-GUID-Schlüssel unter HKCR \\ AppId.

</dd> <dt>

<span id="RemoteServerName"></span><span id="remoteservername"></span><span id="REMOTESERVERNAME"></span>RemoteServerName
</dt> <dd>

Diese Spalte enthält den Wert von "RemoteServerName"=, der <xxxx> unter HKCR \\ AppID \\ {AppID} geschrieben \\ wird.

</dd> <dt>

<span id="LocalService"></span><span id="localservice"></span><span id="LOCALSERVICE"></span>Localservice
</dt> <dd>

Diese Spalte enthält den Wert von LocalService, der unter HKCR \\ AppID \\ { } <appid> "LocalService"= geschrieben <xxx> wird.

</dd> <dt>

<span id="ServiceParameters"></span><span id="serviceparameters"></span><span id="SERVICEPARAMETERS"></span>ServiceParameters
</dt> <dd>

Diese Spalte enthält den Wert von ServiceParameters, der unter HKCR \\ AppID \\ {appid>} "ServiceParameters" geschrieben wird.

</dd> <dt>

<span id="DllSurrogate"></span><span id="dllsurrogate"></span><span id="DLLSURROGATE"></span>DllSurrogate
</dt> <dd>

Diese Spalte enthält den Wert von DllSurrogate, der unter HKCR \\ AppId \\ { } <appid> "DllSurrogate"= geschrieben <xxx> wird. Wenn diese Spalte vorhanden ist, handelt es sich in der Regel um eine leere Zeichenfolge.

</dd> <dt>

<span id="ActivateAtStorage"></span><span id="activateatstorage"></span><span id="ACTIVATEATSTORAGE"></span>ActivateAtStorage
</dt> <dd>

Ein ganzzahliger Wert ungleich 0 in diesem Feld bewirkt, dass Windows Installer HKCR \\ AppID \\ { } <appid> "ActivateAtStorage"="Y" in die Registrierung schreibt. Wenn das Feld leer gelassen wird oder den Wert 0 hat, wird kein Wert geschrieben.

</dd> <dt>

<span id="RunAsInteractiveUser"></span><span id="runasinteractiveuser"></span><span id="RUNASINTERACTIVEUSER"></span>RunAsInteractiveUser
</dt> <dd>

Ein ganzzahliger Wert ungleich 0 in diesem Feld bewirkt, dass Windows Installer HKCR \\ AppID \\ {appid>} "RunAs"="Interactive User" in die Registrierung schreibt. Wenn das Feld leer gelassen wird oder den Wert 0 hat, wird kein Wert geschrieben.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Tabelle wird von der [RegisterClassInfo-Aktion](registerclassinfo-action.md) und der [UnregisterClassInfo-Aktion](unregisterclassinfo-action.md)verwendet.

Beachten Sie, dass die Tabelle AppId keine Spalte zum Registrieren eines Standardnamens enthält. In Fällen, in denen Sie einen benutzerfreundlichen Namen als Wert für Standardname schreiben müssen, müssen Sie sich daher mithilfe der [Registrierungstabelle](registry-table.md)registrieren.

## <a name="validation"></a>Überprüfung

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE33](ice33.md)  
[ICE46](ice46.md)  
[ICE69](ice69.md)  
</dl>

 

 



