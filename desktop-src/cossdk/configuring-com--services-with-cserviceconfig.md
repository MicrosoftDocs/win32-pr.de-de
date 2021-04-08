---
description: Konfigurieren von COM+-Diensten mit cserviceconfig
ms.assetid: c44743a8-8b91-4e2a-9ba4-4cb6ae787999
title: Konfigurieren von COM+-Diensten mit cserviceconfig
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc8bbc6c3131347f450340863db70fd9b3999730
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748049"
---
# <a name="configuring-com-services-with-cserviceconfig"></a>Konfigurieren von COM+-Diensten mit cserviceconfig

Die [**cserviceconfig**](cserviceconfig.md) -Klasse wird verwendet, um die com+-Dienste zu konfigurieren, die ohne Komponenten verwendet werden können. Er aggregiert den frei Thread-Mars Haller und kann daher in verschiedenen Apartments verwendet werden. Um einen einzelnen Dienst zu konfigurieren, müssen Sie [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) für die dem Dienst zugeordnete-Schnittstelle aufzurufen und dann Methoden für diese Schnittstelle aufzurufen, um die entsprechende Konfiguration einzurichten. In der folgenden Tabelle werden die Schnittstellen beschrieben, die durch die **cserviceconfig** -Klasse implementiert werden.



| Schnittstelle                                                                         | BESCHREIBUNG                                                                                                                                                                                              |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Iserviceingeerbanceconfig**](/windows/desktop/api/ComSvcs/nn-comsvcs-iserviceinheritanceconfig)<br/>         | Die Standardschnittstelle für die-Klasse. Es wird verwendet, um viele der com+-Dienste schnell zu initialisieren.<br/>                                                                                              |
| [**Iservicecomtiintrinsicsconfig**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicecomtiintrinsicsconfig)<br/> | Wird verwendet, um die systeminternen Informationen zu COM Transaction Integrator (COMTI) zu konfigurieren. Mit COMTI können Entwickler Mainframe-basierte Transaktions Programme in komponentenbasierte Anwendungen integrieren.<br/> |
| [**Iserviceiisintrinsicsconfig**](/windows/desktop/api/ComSvcs/nn-comsvcs-iserviceiisintrinsicsconfig)<br/>     | Wird verwendet, um die systeminternen Informationen zu Internetinformationsdienste (IIS) zu konfigurieren.<br/>                                                                                                             |
| [**Iservicepartitionconfig**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicepartitionconfig)<br/>             | Wird verwendet, um zu konfigurieren, wie COM+-Partitionen mit den Diensten verwendet werden.<br/>                                                                                                                             |
| [**Iservicesxsconfig**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicesxsconfig)<br/>                         | Wird verwendet, um parallele Assemblys zu konfigurieren.<br/>                                                                                                                                                    |
| [**Iservicesynchronizationconfig**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicesynchronizationconfig)<br/> | Wird zum Konfigurieren der com+-Synchronisierungs Dienste verwendet.<br/>                                                                                                                                              |
| [**Iservicethreadpoolconfig**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicethreadpoolconfig)<br/>           | Wird verwendet, um den Thread Pool für den com+-Dienst zu konfigurieren. Der Thread Pool kann nur konfiguriert werden, wenn die [**cokreateactivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) -Funktion verwendet wird.<br/>                          |
| [**Iservicetrackerconfig**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicetrackerconfig)<br/>                 | Wird zum Konfigurieren der Tracker-Eigenschaft verwendet. Tracker ist ein Berichtsmechanismus, der von der Überwachung des Codes verwendet wird, um zu beobachten, welcher Code ausgeführt wird.<br/>                                                         |
| [**Iservicetransaktionconfig**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicetransactionconfig)<br/>         | Wird verwendet, um den com+-Transaktions Dienst zu konfigurieren.<br/>                                                                                                                                               |



 

## <a name="component-services-administrative-tool"></a>Verwaltungs Tool für Komponenten Dienste

Nicht anwendbar.

## <a name="visual-basic"></a>Visual Basic

Nicht anwendbar.

## <a name="cc"></a>C/C++

Das folgende Code Fragment veranschaulicht, wie ein [**cserviceconfig**](cserviceconfig.md) -Objekt erstellt und konfiguriert wird, um com+-Transaktionen zu verwenden.


```C++
// Create a CServiceConfig object.
HRESULT hr = CoCreateInstance(CLSID_CServiceConfig, NULL, CLSCTX_INPROC_SERVER, 
  IID_IUnknown, (void**)&pUnknownCSC);
if (FAILED(hr)) throw(hr);

// Query for the IServiceInheritanceConfig interface.
hr = pUnknownCSC->QueryInterface(IID_IServiceInheritanceConfig, 
  (void**)&pInheritanceConfig);
if (FAILED(hr)) throw(hr);

// Inherit the current context before using transactions.
hr = pInheritanceConfig->ContainingContextTreatment(CSC_Inherit);
if (FAILED(hr)) throw(hr);

// Query for the IServiceTransactionConfig interface.
hr = pUnknownCSC->QueryInterface(IID_IServiceTransactionConfig, 
  (void**)&pTransactionConfig);
if (FAILED(hr)) throw(hr);

// Configure transactions to always create a new one.
hr = pTransactionConfig->ConfigureTransaction(CSC_NewTransaction);
if (FAILED(hr)) throw(hr);

// Set the isolation level of the transactions to ReadCommitted.
hr = pTransactionConfig->IsolationLevel( 
  COMAdminTxIsolationLevelReadCommitted);
if (FAILED(hr)) throw(hr);

// Set the transaction time-out to 1 minute.
hr = pTransactionConfig->TransactionTimeout(60);
if (FAILED(hr)) throw(hr);

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Cserviceconfig**](cserviceconfig.md)
</dt> <dt>

[Verwenden von COM+-Diensten über cokreateactivity](using-com--services-through-cocreateactivity.md)
</dt> <dt>

[Verwenden von COM+-Diensten über coenterservicedomain und coleaveservicedomain](using-com--services-through-coenterservicedomain-and-coleaveservicedomain.md)
</dt> </dl>

 

