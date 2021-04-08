---
description: Die AppID-Tabelle oder die Registrierungs Tabelle gibt an, dass das Installationsprogramm DCOM-Server konfiguriert und registriert, um einen der folgenden Schritte während einer Installation durchzuführen.
ms.assetid: d76ed6df-944b-4996-bf07-e42ceb7a1b69
title: AppID-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07fa202907c094d8c12f73d838f5ad1d6b942125
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864491"
---
# <a name="appid-table"></a>AppID-Tabelle

Die AppID-Tabelle oder die [Registrierungs Tabelle](registry-table.md) gibt an, dass das Installationsprogramm DCOM-Server konfiguriert und registriert, um einen der folgenden Schritte während einer Installation durchzuführen.

-   Führt den DCOM-Server unter einer anderen Identität aus als der Benutzer, der den Server aktiviert. Beispielsweise, um einen DCOM-Server so zu konfigurieren, dass er immer als interaktiver Benutzer oder als vordefinierter Benutzer ausgeführt wird.
-   Führen Sie den DCOM-Server als Dienst aus.
-   Konfigurieren Sie den Standard Sicherheits Zugriff für den DCOM-Server.
-   Registrieren Sie den DCOM-Server so, dass er auf einem anderen Computer aktiviert ist.

Diese Tabelle wird bei der Installation der Komponente verarbeitet, die dem DCOM-Server in der \_ Spalte Komponente der [Klassen Tabelle](class-table.md)zugeordnet ist. Eine AppID wird nicht angekündigt.

Die AppID-Tabelle weist die folgenden Spalten auf.



| Spalte               | Typ                       | Schlüssel | Nullwerte zulässig |
|----------------------|----------------------------|-----|----------|
| AppId                | [GUID](guid.md)           | J   | N        |
| RemoteServerName     | [Großformatige](formatted.md) | N   | J        |
| LocalService         | [Text](text.md)           | N   | J        |
| Service Parameters    | [Text](text.md)           | N   | J        |
| Dllersatz         | [Text](text.md)           | N   | J        |
| Activateatstorage    | [Integer](integer.md)     | N   | J        |
| Runasinteractiveuser | [Integer](integer.md)     | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="AppId"></span><span id="appid"></span><span id="APPID"></span>AppID
</dt> <dd>

Die AppID-Spalte der [Klassen Tabelle](class-table.md) ist ein Fremdschlüssel in diese Spalte der AppID-Tabelle. Diese Spalte enthält den AppID-Wert, der unter der CLSID geschrieben wird, und erstellt den AppID-GUID-Schlüssel unter HKCR \\ AppID.

</dd> <dt>

<span id="RemoteServerName"></span><span id="remoteservername"></span><span id="REMOTESERVERNAME"></span>Remote Servername
</dt> <dd>

Diese Spalte enthält den Wert von "Remoteservername" = <xxxx> , der unter HKCR \\ AppID \\ {AppID} geschrieben wird \\ .

</dd> <dt>

<span id="LocalService"></span><span id="localservice"></span><span id="LOCALSERVICE"></span>LocalService
</dt> <dd>

Diese Spalte enthält den Wert von LocalService, der unter HKCR \\ AppID \\ { <appid> } "LocalService" = geschrieben wird <xxx> .

</dd> <dt>

<span id="ServiceParameters"></span><span id="serviceparameters"></span><span id="SERVICEPARAMETERS"></span>Service Parameters
</dt> <dd>

Diese Spalte enthält den Wert von Service Parameters, der unter HKCR \\ AppID \\ {AppID>} "Service Parameters" geschrieben wird.

</dd> <dt>

<span id="DllSurrogate"></span><span id="dllsurrogate"></span><span id="DLLSURROGATE"></span>Dllersatz
</dt> <dd>

Diese Spalte enthält den Wert von dllersatz, der unter HKCR \\ AppID \\ { <appid> } "dllersatz" = geschrieben wird <xxx> . Wenn diese Spalte vorhanden ist, handelt es sich in der Regel um eine leere Zeichenfolge.

</dd> <dt>

<span id="ActivateAtStorage"></span><span id="activateatstorage"></span><span id="ACTIVATEATSTORAGE"></span>Activateatstorage
</dt> <dd>

Ein ganzzahliger Wert ungleich 0 (null) in diesem Feld bewirkt, dass Windows Installer HKCR \\ AppID \\ { <appid> } "activateatstorage" = "Y" in die Registrierung schreibt. Wenn das Feld leer gelassen wird oder den Wert 0 (null) aufweist, wird kein Wert geschrieben.

</dd> <dt>

<span id="RunAsInteractiveUser"></span><span id="runasinteractiveuser"></span><span id="RUNASINTERACTIVEUSER"></span>Runasinteractiveuser
</dt> <dd>

Ein ganzzahliger Wert ungleich 0 (null) in diesem Feld bewirkt, dass Windows Installer HKCR \\ AppID \\ {AppID>} "runas" = "Interactive User" in die Registrierung schreibt. Wenn das Feld leer gelassen wird oder den Wert 0 (null) aufweist, wird kein Wert geschrieben.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Tabelle wird von der [RegisterClassInfo-Aktion](registerclassinfo-action.md) und der [unregisterclassinfo-Aktion](unregisterclassinfo-action.md)verwendet.

Beachten Sie, dass die AppID-Tabelle keine Spalte zum Registrieren eines Standard namens enthält. In Fällen, in denen Sie einen benutzerfreundlichen Namen als Standardwert für den Namen schreiben müssen, müssen Sie sich daher mithilfe der [Registrierungs Tabelle](registry-table.md)registrieren.

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE33](ice33.md)  
[ICE46](ice46.md)  
[ICE69](ice69.md)  
</dl>

 

 



