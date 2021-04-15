---
description: Definiert den Typ von Endpunkten, die zum Herstellen einer Verbindung mit einem Dienst verwendet werden können.
ms.assetid: 50397D25-7C71-4AA2-89BF-F90CBDCFFA91
title: Updateendpointtype-Enumeration (updateendpointauth. h)
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
ms.openlocfilehash: 942bcb5275c6a4f39d6e2828025e5b9a40e52c46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525073"
---
# <a name="updateendpointtype-enumeration"></a>Updateendpointtype-Enumeration

Definiert den Typ von Endpunkten, die zum Herstellen einer Verbindung mit einem Dienst verwendet werden können.

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

<span id="uetClientServer"></span><span id="uetclientserver"></span><span id="UETCLIENTSERVER"></span>**uetclientserver**
</dt> <dd>

Ein Client/Server-Endpunkt, der zum Herstellen der Verbindung mit dem Aktualisierungs Dienst verwendet wird, z. b. Windows Update, Microsoft Update und WSUS-Server in einer Unternehmensumgebung, um Informationen zu Updates zu erhalten, die möglicherweise für den Computer gelten.

Der Aktualisierungs Dienst gibt Informationen zu Updates zurück, die seit der letzten Synchronisierung des Clients mit dem Server veröffentlicht, überarbeitet oder zurückgezogen wurden.

</dd> <dt>

<span id="uetReporting"></span><span id="uetreporting"></span><span id="UETREPORTING"></span>**uetreporting**
</dt> <dd>

Ein Berichterstattungs Endpunkt, der verwendet wird, wenn der Client die Ergebnisse von Scans, Downloads und Installationen zurück an den Aktualisierungs Dienst meldet.

Im Fall von öffentlichen Diensten (Windows Update und Microsoft Update) erfolgt dies für Qualitäts Überwachungszwecke.

Bei privaten Diensten, z. b. bei einem WSUS-Server des Unternehmens, kann der Server mit thhis-Endpunkt auch Inventur Daten und andere Informationen zu den Client Computern, die verwaltet werden, erfassen.

</dd> <dt>

<span id="uetWuaSelfUpdate"></span><span id="uetwuaselfupdate"></span><span id="UETWUASELFUPDATE"></span>**uetwuaselfupdate**
</dt> <dd>

Ein selbst Aktualisierungs Endpunkt, der verwendet wird, wenn der Client Computer einen Update Dienst kontaktiert, um festzustellen, ob eine neue Version der Windows Update-Agent-Client Software vorhanden ist.

Der Self-Update-Endpunkt verwendet ein anderes Protokoll als den Client-Server Endpunkt, sodass selbst Updates verteilt werden können, auch wenn es einen Fehlerzustand gibt, der möglicherweise verhindert, dass die normale Client/Server-Synchronisierung auf einem bestimmten Client Computer funktioniert.

</dd> <dt>

<span id="uetRegulation"></span><span id="uetregulation"></span><span id="UETREGULATION"></span>**uetregulations**
</dt> <dd>

Ein-Regel Endpunkt, der verwendet wird, wenn der Client Computer eine Verbindung mit dem-Verwaltungs Endpunkt hergestellt hat, um ein bestimmtes Update zu ergreifen, das auf den Zielcomputer anwendbar ist.

Der-Regulierungs Dienst kann angeben, ob das Update "reguliert" (auch als "gedrosselt" bezeichnet) – mit anderen Worten: der-Regulierungs Dienst kann dem Client Computer mitteilen, dass er nicht auf ein bestimmtes Update angewendet werden soll, obwohl dieses Update zutreffend ist.

</dd> <dt>

<span id="uetSimpleTargeting"></span><span id="uetsimpletargeting"></span><span id="UETSIMPLETARGETING"></span>**uetsimpletargeting**
</dt> <dd>

Ein Endpunkt für die einfache Ausrichtung, der nur mit privaten Diensten (WSUS-Server in Unternehmensumgebungen) verwendet wird. In einer Unternehmensumgebung können Client Computer bestimmten Zielgruppen zugewiesen werden, und Updates können für die Installation auf Computern in einigen Gruppen, aber nicht für andere Personen genehmigt werden.

Beispielsweise kann der WSUS-Administrator eine "Test"-Gruppe für Computer erstellen, die zum Testen neuer Updates verwendet werden, und der Administrator kann neu veröffentlichte Updates für die Installation auf Computern in der Testgruppe genehmigen, ohne Sie für die Installation auf anderen Computern in der Organisation genehmigen zu müssen. Die einfache Zielgruppe wird verwendet, um einem Client Computer die Registrierung beim WSUS-Server zu ermöglichen und dem Server zu gestatten, dem Client Computer mitzuteilen, in welcher Gruppe er sich befindet.

</dd> <dt>

<span id="uetSecuredClientServer"></span><span id="uetsecuredclientserver"></span><span id="UETSECUREDCLIENTSERVER"></span>**uetsecuredclientserver**
</dt> <dd>

Einen gesicherten Client/Server-Endpunkt, mit dem ein Client Informationen zu apps abrufen kann, die eine Lizenzierung benötigen, damit Sie auf einem Client Computer verwendet werden können. Dieses Lizenzierungs Framework wird zurzeit nur von Windows 8 verwendet, um apps und Updates bereitzustellen, die über den Windows Store abgerufen werden. Der gesicherte Client-Server-Endpunkt wird derzeit nicht von Windows Update, Microsoft Update oder WSUS verwendet.

</dd> <dt>

<span id="uetSecondaryServiceAuth"></span><span id="uetsecondaryserviceauth"></span><span id="UETSECONDARYSERVICEAUTH"></span>**uetsecondaryserviceauth**
</dt> <dd>

Der Endpunkt für die sekundäre Dienst Authentifizierung wird von einem Client verwendet, um die Authentifizierung bereitzustellen, bevor er Informationen zu apps erhält, die eine Lizenzierung benötigen, damit Sie auf einem Client Computer verwendet werden können. Dieses Lizenzierungs Framework wird derzeit nur von Windows 8 verwendet, um apps und Updates bereitzustellen, die über den Windows Store abgerufen werden. Der Endpunkt für die sekundäre Dienst Authentifizierung wird derzeit von Windows Update, Microsoft Update oder WSUS nicht verwendet.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                              |
| Header<br/>                   | <dl> <dt>Updateendpointauth. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Updateendpointauth. idl</dt> </dl> |



 

 




