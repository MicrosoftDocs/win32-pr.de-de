---
description: Proxy Locator-Konfigurationseinstellungen
ms.assetid: d74a85cf-293e-4322-9aff-55b06d6fda5e
title: Proxy Locator-Konfigurationseinstellungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3503a90bcccc990865769b6bf02a65fc383511f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130485"
---
# <a name="proxy-locator-configuration-settings"></a>Proxy Locator-Konfigurationseinstellungen

In diesem Thema werden die Konfigurationseinstellungen für den standardproxylocator beschrieben. Weitere Informationen zum Erstellen des proxylocators mit benutzerdefinierten Konfigurationseinstellungen finden [Sie unter Konfigurieren des proxylocators](how-to-configure-the-proxy-locator.md).

Der proxylocator kann für den Betrieb in drei Modi konfiguriert werden: *manueller Modus*, *Modus für automatische Erkennung* und *Browsermodus*. Die Werte werden in der [**MF- \_ proxysettings**](/windows/desktop/api/mfidl/ne-mfidl-mfnet_proxysettings) -Enumeration definiert. Die Anwendung kann den Modus konfigurieren, indem Sie die Eigenschaft [**MF NetSource \_ proxysettings**](mfnetsource-proxysettings-property.md) festlegt. Der proxylocator kann auch so konfiguriert werden, dass kein Proxy Server verwendet wird, indem diese Eigenschaft auf **mfnet \_ proxysetting \_ None** festgelegt wird. Der Proxy Server wird nicht verwendet, wenn es sich bei dem Medienserver um einen lokalen Host handelt, oder die Anwendung fordert eine Adresse (127. x. x. x) an, die für Loopback Tests reserviert ist –.

> [!Caution]  
> Ein Proxy Server ist eine Sicherheitsbarriere zwischen Ihrem Intranet und dem Internet. Wenn Sie keinen Proxy Server verwenden, kann das Netzwerk Sicherheitsbedrohungen ausgesetzt sein.

 

-   Manueller Modus. Die Anwendung legt diesen Modus fest, indem die [**mfnetsource \_ proxysetting**](mfnetsource-proxysettings-property.md) -Eigenschaft auf **mfnet \_ proxysetting \_ Manual** festgelegt wird. Die Anwendung muss die folgenden Verbindungsinformationen angeben:

    -   Hostname des Proxy Servers: [**MF NetSource \_ proxyhostname**](mfnetsource-proxyhostname-property.md) -Eigenschaft.
    -   Port Nummer: [**MF NetSource \_ ProxyPort**](mfnetsource-proxyport-property.md) -Eigenschaft.
    -   Gibt an, ob ein Proxy Server für lokale Adressen verwendet werden soll: [**mfnetsource \_ proxybypassforlocal**](mfnetsource-proxybypassforlocal-property.md) -Eigenschaft. Diese Einstellung ist optional. Wenn dies nicht angegeben ist, verwendet der proxylocator den Standardwert **false**.

        > [!Note]  
        > Wenn Sie den Proxy Server umgehen, kann die Anwendung schneller eine Verbindung mit Medienservern im Intranet herstellen.

         

    -   Liste der Medienserver Adressen, für die kein Proxy Server zum Herstellen einer Verbindung erforderlich ist: [**mfnetsource \_ proxyexceptionlist**](mfnetsource-proxyexceptionlist-property.md) -Eigenschaft. Diese Einstellung ist optional.

-   Modus zur automatischen Erkennung. Die Anwendung legt diesen Modus fest, indem die [**mfnetsource \_ proxysetting**](mfnetsource-proxysettings-property.md) -Eigenschaft auf **mfnet \_ proxysetting \_ Auto** festgelegt wird. In diesem Modus verwendet der proxylocator den WinHTTP AutoProxy-Mechanismus, um den Hostnamen und die Portnummer für den Proxy Server zu erhalten. Diese Verbindungsinformationen werden mithilfe des automatischen WPAD-Proxy Skripts abgerufen, das vom Domänen Administrator konfiguriert wird. Weitere Informationen zu diesem Mechanismus finden Sie auf der [Microsoft-Website](../winhttp/winhttp-autoproxy-support.md).

    Der proxylocator speichert die Verbindungsinformationen in der Registrierung zwischen. Bei nachfolgenden Proxy Erkennungs aufrufen liest der proxylocator Proxy Informationen aus dem Registrierungs Cache, um den bei der automatischen Erkennung beteiligten Verwaltungsaufwand zu verringern. Die Anwendung kann jedoch die erneute Erkennung des automatischen Proxys erzwingen, indem Sie die Eigenschaft [**MF NetSource \_ proxyrerunautoerkennungs**](mfnetsource-proxyrerunautodetection-property.md) festlegt.

-   Browser Modus. Die Anwendung legt diesen Modus fest, indem die [**mfnetsource \_ proxysetting**](mfnetsource-proxysettings-property.md) -Eigenschaft auf **mfnet \_ proxysetting- \_ Browser** festgelegt wird. In diesem Modus verwendet der proxylocator die Proxy Einstellungen der Browser Anwendung. Dieser Modus wird standardmäßig festgelegt, wenn das Protokoll http oder httpd ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Proxy Unterstützung für Netzwerk Quellen](proxy-support-for-network-sources.md)
</dt> </dl>

 

 
