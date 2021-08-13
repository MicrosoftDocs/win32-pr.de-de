---
description: Definiert den Typ der Endpunkte, die zum Herstellen einer Verbindung mit einem Dienst verwendet werden können.
ms.assetid: 50397D25-7C71-4AA2-89BF-F90CBDCFFA91
title: UpdateEndpointType-Enumeration (UpdateEndpointAuth.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UpdateEndpointType
api_type:
- HeaderDef
api_location:
- UpdateEndpointAuth.h
ms.openlocfilehash: 7fbfd67b3009fbe904284ea7a92cdea996d0a6e23a43a17639eb567d66536917
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119462910"
---
# <a name="updateendpointtype-enumeration"></a>UpdateEndpointType-Enumeration

Definiert den Typ der Endpunkte, die zum Herstellen einer Verbindung mit einem Dienst verwendet werden können.

## <a name="syntax"></a>Syntax


```C++
typedef enum tagEndpointType { 
  uetClientServer          = 0,
  uetReporting             = ( uetClientServer + 1 ),
  uetWuaSelfUpdate         = ( uetReporting + 1 ),
  uetRegulation            = ( uetWuaSelfUpdate + 1 ),
  uetSimpleTargeting       = ( uetRegulation + 1 ),
  uetSecuredClientServer   = ( uetSimpleTargeting + 1 ),
  uetSecondaryServiceAuth  = ( uetSecuredClientServer + 1 )
} UpdateEndpointType;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="uetClientServer"></span><span id="uetclientserver"></span><span id="UETCLIENTSERVER"></span>**uetClientServer**
</dt> <dd>

Ein Client-Server-Endpunkt, der verwendet wird, um eine Verbindung mit dem Updatedienst herzustellen, z. B. Windows Update, Microsoft Update und WSUS-Server in einer Unternehmensumgebung, um Informationen zu Updates zu finden, die möglicherweise auf den Computer anwendbar sind.

Der Updatedienst gibt Informationen zu Updates zurück, die seit der letzten Synchronisierung des Clients mit dem Server veröffentlicht, überarbeitet oder eingestellt wurden.

</dd> <dt>

<span id="uetReporting"></span><span id="uetreporting"></span><span id="UETREPORTING"></span>**uetReporting**
</dt> <dd>

Ein Berichtsendpunkt, der verwendet wird, wenn der Client die Ergebnisse von Überprüfungen meldet, herunterlädt und wieder an den Updatedienst installiert.

Bei öffentlichen Diensten (Windows Update und Microsoft Update) erfolgt dies zu Qualitätsüberwachungszwecken.

Bei privaten Diensten, z. B. einem WSUS-Unternehmensserver, ermöglicht der thhis-Endpunkttyp dem Server auch das Sammeln von Inventur- und anderen Informationen zu den Clientcomputern, die von der Verwaltung verwendet werden.

</dd> <dt>

<span id="uetWuaSelfUpdate"></span><span id="uetwuaselfupdate"></span><span id="UETWUASELFUPDATE"></span>**uetWuaSelfUpdate**
</dt> <dd>

Ein Selbstupdateendpunkt, der verwendet wird, wenn der Clientcomputer einen Updatedienst kontaktiert, um festzustellen, ob eine neue Version der Windows Update-Agent-Clientsoftware vorhanden ist.

Der Self-Update-Endpunkt verwendet ein anderes Protokoll als der Client-Server Endpunkt, sodass Selbstupdates auch dann verteilt werden können, wenn eine Fehlerbedingung vorliegt, die möglicherweise verhindert, dass die normale Client-Server-Synchronisierung auf einem bestimmten Clientcomputer funktioniert.

</dd> <dt>

<span id="uetRegulation"></span><span id="uetregulation"></span><span id="UETREGULATION"></span>**uetRegulation**
</dt> <dd>

Ein Regulierungsendpunkt, der verwendet wird, wenn der Clientcomputer den Regulierungsdienst kontaktiert, um auf ein bestimmtes Update zu reagieren, das auf den Zielcomputer anwendbar ist.

Der Regulierungsdienst kann angeben, ob das Update "reguliert" ist (auch als "gedrosselt" bezeichnet). Anders ausgedrückt: Der Regulierungsdienst kann dem Clientcomputer mitteilen, dass er nicht auf ein bestimmtes Update reagieren soll, obwohl dieses Update anscheinend anwendbar ist.

</dd> <dt>

<span id="uetSimpleTargeting"></span><span id="uetsimpletargeting"></span><span id="UETSIMPLETARGETING"></span>**uetSimpleTargeting**
</dt> <dd>

Ein Endpunkt mit einfacher Zielgruppenadressierung, der nur mit privaten Diensten (WSUS-Server in Unternehmensumgebungen) verwendet wird. In einer Unternehmensumgebung können Clientcomputer bestimmten Zielgruppen zugewiesen werden, und Updates können für die Installation auf Computern in einigen Gruppen genehmigt werden, aber nicht für andere.

Beispielsweise kann der WSUS-Administrator eine Testgruppe für Computer erstellen, die zum Testen neuer Updates verwendet werden, und der Administrator kann neu veröffentlichte Updates für die Installation auf Computern in der Testgruppe genehmigen, ohne sie für die Installation auf anderen Computern in der Organisation zu genehmigen. Der einfache Zielaustausch wird verwendet, um einem Clientcomputer die Registrierung beim WSUS-Server zu ermöglichen und dem Server zu ermöglichen, dem Clientcomputer mitzuteilen, in welcher Gruppe er sich befindet.

</dd> <dt>

<span id="uetSecuredClientServer"></span><span id="uetsecuredclientserver"></span><span id="UETSECUREDCLIENTSERVER"></span>**uetSecuredClientServer**
</dt> <dd>

Ein geschützter Clientserverendpunkt, der es einem Client ermöglicht, Informationen zu Apps abzurufen, die lizenziert werden müssen, damit sie auf einem Clientcomputer verwendet werden können. Dieses Lizenzierungsframework wird derzeit nur von Windows 8 verwendet, um Apps und Updates bereitzustellen, die über die Windows Store abgerufen werden. Der gesicherte Clientserverendpunkt wird derzeit nicht von Windows Update, Microsoft Update oder WSUS verwendet.

</dd> <dt>

<span id="uetSecondaryServiceAuth"></span><span id="uetsecondaryserviceauth"></span><span id="UETSECONDARYSERVICEAUTH"></span>**uetSecondaryServiceAuth**
</dt> <dd>

Der sekundäre Dienstauthentifizierungsendpunkt wird von einem Client verwendet, um eine Authentifizierung bereitzustellen, bevor er Informationen zu Apps erhält, die lizenziert werden müssen, damit sie auf einem Clientcomputer verwendet werden können. Dieses Lizenzierungsframework wird derzeit nur von Windows 8 verwendet, um Apps und Updates bereitzustellen, die über die Windows Store abgerufen werden. Der Sekundärdienstauthentifizierungsendpunkt wird derzeit nicht von Windows Update, Microsoft Update oder WSUS verwendet.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                        |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                              |
| Header<br/>                   | <dl> <dt>UpdateEndpointAuth.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>UpdateEndpointAuth.idl</dt> </dl> |



 

 




